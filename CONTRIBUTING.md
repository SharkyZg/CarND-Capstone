Introduction
============

This document summarizes the general guidelines for contributing to this project.

Basic Workflow
==============

Every developer should follow the following workflow when contributing to the
project:

Initial setup
-------------

To setup your environment, clone the
[team's repository](https://github.com/CarND-EuroBots/CarND-Capstone):

    $ git clone git@github.com:CarND-EuroBots/CarND-Capstone.git

Contribute
----------

To add some changes to the repository, follow these steps:

1. Go to the cloned repository from the previous step:

       $ cd CarND-Capstone

2. Go to the master branch:

       $ git checkout master

3. Create a new branch for your changes:

       $ git checkout -b <my_branch>

   **NOTE**: always create a new branch for your changes.
   Keep one branch per change; do not mix different changes in the same branch.

4. Make changes.

5. Add changes:

       $ git add <files that changed>

6. Commit them:

       $ git commit

   **NOTE**: see the `Commit messages` section below on how to write a
   valid commit message.

7. Push your changes:

       $ git push origin <my_branch>

8. From the GitHub user interface, click on `New Pull Request` from
   `<CarND-Eurobots/CarND-Capstone:<my_branch>` to
   `<CarND-Eurobots/CarND-Capstone:master`.

9. Repeat steps from 4 if you wish to add more changes.

   **NOTE**: do **not** edit or squash your commits.

10. Wait until the Travis job validates your changes.

11. Wait until someone reviews your PR, especially if you are
    modifying other person's code.

12. Merge pull request and delete branch.

Updating from upstream
----------------------
To get changes from the team's contributors, simply run:

    $ git pull origin master

Updating from Udacity's upstream
--------------------------------

To get changes from Udacity, follow these steps:

1. Add Udacity's repository as a remote:

       $ git remote add upstream https://github.com/udacity/CarND-Capstone.git

2. Go to your master branch:

       $ git checkout master

3. Pull the changes from `upstream`:

       $ git pull upstream master

4. Fix merge conflicts, if any.

5. Push these changes to the team's repository:

       $ git push origin master

Commit size
===========

If possible, create **small**, focused pull requests with small changes,
in order to speed up the code-review process.

Changes should, if possible, be under 100 lines of code.

Commit messages
===============

The commit message must fulfill the
[seven rules of a great Git commit message](https://chris.beams.io/posts/git-commit/):

* Separate subject from body with a blank line.
* Limit the subject line to 50 characters.
* Capitalize the subject line.
* Do not end the subject line with a period.
* Use the imperative mood in the subject line. 
  The commit message should fit in the sentence:

      This commit will <commit_message>

* Wrap the body at 72 characters.
* Use the body to explain _what_ and _why_, not _how_.

Code Style
==========

We are currently using `pycodestyle` to check our Python code style, and
it's verified in our Travis CI system.

Before pushing your code, make sure you pass the code style check by running:

    $ python pyjobs/pycodestyle.py
