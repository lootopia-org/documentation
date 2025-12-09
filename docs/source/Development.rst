Development
===

Overview
--------
This guide outlines the complete development workflow for our organization, 
from repository creation to production deployment. 
Following these practices ensures code quality, proper review processes, and safe deployments.

Repository Management
---------------------
One Repository Per Service
~~~~~~~~~~~~~~~~~~~~~~~~~~
Each microservice, application, or independent component must have its own dedicated repository. This approach provides:

- Clear ownership: Each service has distinct maintainers and responsibilities
- Independent versioning: Services can be versioned and released independently
- Reduced complexity: Smaller codebases are easier to understand and maintain
- Isolated CI/CD: Each service has its own build and deployment pipeline

Examples of what constitutes a separate service:

- User authentication service
- Payment processing API
- Frontend web application
- Mobile backend API
- Data processing worker

Branches
--------
Branch protection is configured on the production branch so that it can never be pushed on directly,
Here are the rules that are configured on the branches

- Require pull request reviews before merging
- Require status checks to pass
- Disable force pushes
- Restrict who can push directly (typically no one)


Branch Hierarchy
~~~~~~~~~~~~~~~~

Our workflow uses four primary branch types in this order:

1. **Feature branches**: Individual development work
2. **dev**: Development integration environment
3. **int**: Integration/staging environment
4. **prod**: Production environment

The Complete Flow
~~~~~~~~~~~~~~~~~

::

   feature-branch → dev → int → prod
        (PR)        (PR)   (PR)

Each arrow represents a pull request with code review and automated checks.

Step-by-Step Workflow
---------------------

Step 1: Starting New Work
~~~~~~~~~~~~~~~~~~~~~~~~~

Always create a feature branch from the latest ``dev`` branch:

.. code-block:: bash

   # Ensure you're on dev and it's up to date
   git checkout dev
   git pull origin dev

   # Create your feature branch
   git checkout -b feature/{ticket_id}_{verb}-{feature}
   ex: git checkout -b feature/PE-123_add-user-authentication

Branch naming best practices:
 
- Use prefixes: ``feature/``, ``bugfix/``, ``hotfix/``
- Include ticket/issue numbers
- Be descriptive: ``feature/oauth-integration`` not ``feature/update``
- Use lowercase with hyphens

Step 2: Developing Your Feature
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Make your changes and commit regularly:

.. code-block:: bash

   # Make your changes
   # Edit files, write code, add tests

   # Check what changed
   git status
   git diff

   # Stage your changes
   git add src/auth/login.js
   git add tests/auth/login.test.js

   # Or stage all changes
   git add .

   # Commit with a descriptive message
   git commit -m "chore: add OAuth 2.0 authentication flow

   - Implement OAuth provider integration
   - Add token validation middleware
   - Include unit tests for auth flow
   - Update API documentation"

   # Push to remote regularly
   git push origin feature/PE-123_add-user-authentication

Commit message guidelines:

- First word: must be a label
- the word after the label must be a word
- First line: Brief summary (50 chars or less)
- Blank line
- Detailed description of what and why
- Reference issue numbers if applicable

.. list-table::
   :widths: 15 35 50
   :header-rows: 1

   * - Commit Type
     - Description
     - When to Use

   * - feat
     - A new feature for the user or system.
     - When adding a new feature or functionality

   * - fix
     - A bug fix.
     - When correcting a defect in the code

   * - chore
     - Routine tasks or maintenance without affecting functionality.
     - When updating build scripts, dependencies, refactoring, or general housekeeping

   * - docs
     - Documentation only changes.
     - When updating README, comments, or docs

   * - style
     - Code style or formatting changes.
     - When fixing whitespace, indentation, or formatting

   * - refactor
     - Code refactoring.
     - When restructuring code without adding features

   * - test
     - Adding or updating tests.
     - When adding new tests or modifying existing ones

   * - perf
     - Performance improvements.
     - When improving performance without adding features


Step 3: Feature Branch to Dev
-----------------------------

Once your feature is complete and tested locally:

.. code-block:: bash

   # Ensure your branch is up to date with dev
   git checkout dev
   git pull origin dev
   git checkout feature/PE-123_add-user-authentication
   git merge dev

   # Resolve any conflicts if they exist
   # Test thoroughly after merge

   # Push your latest changes
   git push origin feature/PE-123_add-user-authentication

Create Pull Request to dev and request a reviewer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Go to your repository on https://github.com/lootopia-org
2. Click "New Pull Request" or "Create Pull Request"
3. Set base branch to dev
4. Set compare branch to your feature branch
5. Fill in the PR template:

.. code-block:: md
  # Description
    Brief description of what this PR does

  # Changes
    - Added OAuth 2.0 authentication
    - Implemented token refresh mechanism
    - Added rate limiting to auth endpoints

  # Testing
    -[x] Unit tests pass locally
    -[] Integration tests pass
    -[] Manually tested the flow
    -[] No breaking changes

  # Related Issues(if Applicable)
    Closes #123
6. Request reviewers
7. Wait for approval and CI/CD checks to pass
8. Merge the PR (usually using "Squash and merge" or "Merge commit")
9. Delete the feature branch after merging


