============
Contributing
============

First off, thanks for taking the time to contribute!

Contributions are welcome by anybody and everybody. We are not kidding! Looking for help ? Join us on `Slack`_ by requesting an `invite`_.

The rest of this document will be guidelines to contributing to a project. Remember that these are just guidelines, not rules. Use common sense as much as possible.

.. _invite: http://pyslackers.com/
.. _Slack: https://pythondev.slack.com/

Pull Request Guidelines
-----------------------

Before you submit a pull request, check that it meets these guidelines:

1. The pull request should include tests (if necessary). If you have any questions about how to write tests then ask the community.
2. If the pull request adds functionality update the docs where appropriate.
3. Use a `good commit message`_.

.. _good commit message: https://github.com/spring-projects/spring-framework/blob/30bce7/CONTRIBUTING.md#format-commit-messages

Types of Contributions
----------------------

Report Bugs
^^^^^^^^^^^

The best way to report a bug is to file an issue via the target project's issue tracker.

Please include:

* Your operating system name and version.
* Any details about your local setup that might be helpful in troubleshooting.
* Detailed steps to reproduce the bug.

Fix Bugs & Features
^^^^^^^^^^^^^^^^^^^

Look through the github issues for bugs or features request.
Anything tagged with "help-wanted" is open to whoever wants to implement it.

Write Documentation
^^^^^^^^^^^^^^^^^^^

Our projects could always use more documentation and examples, whether as part of the
official documentation, in docstrings, or even on the web in blog posts, articles, and such.

Submit Feedback
^^^^^^^^^^^^^^^

The best way to submit feedback is to file an issue via the target project's issue tracker.

If you are proposing a feature:

* Explain in detail how it would work.
* Keep the scope as narrow as possible, to make it easier to implement.
* Remember that these are volunteer-driven projects, and that contributions are welcome :)

Get Started!
------------

Ready to contribute? Here is a our preferred approach to forking our projects:

1. Fork the target project's repo on github.
2. Clone your fork locally and add the upstream repository:

   .. code-block:: console

        $ git clone git@github.com:<your-username>/<project-name>.git <project-name>
        $ git remote add upstream https://github.com/pyslackers/<project-name>.git
        $ cd <project-name>/

3. Refer to the target project's CONTRIBUTING file. It contains the steps required to set up and run its preferred dev environment.

4. Create a branch for local development:

   .. code-block:: console

        $ git checkout -b <name-of-your-bugfix-or-feature>

   Now you can make your changes locally.

5. When you're done making changes, check that your changes pass flake8 and the tests, including testing other Python versions with tox:

   .. code-block:: console

        $ tox

6. Commit your changes and push your branch to github:

    .. code-block:: console

        $ git add .
        $ git commit
        $ git push origin <name-of-your-bugfix-or-feature>

7. Submit a pull request through the github website.

Git Hygiene
-----------

Handling Merge Conflicts
^^^^^^^^^^^^^^^^^^^^^^^^

Occasionally a Pull Request will have Merge Conflicts. **Do not merge master into your branch.** Instead, make sure your ``master`` branch is up to date:

.. code-block:: console

    $ git checkout master
    $ git pull upstream master
    $ git push origin master

Then rebase your branch on ``master``:

.. code-block:: console

    $ git checkout <name-of-your-bugfix-or-feature>
    $ git rebase master

If there are any conflicts you need to resolve, it will suspend the rebase for you to fix them. Then do:

.. code-block:: console

    $ git add .
    $ git rebase --continue

It will do one round of conflict-checking for each commit in your branch, so keeping your history clean will make rebasing much easier. When the rebase is done, your branch will be up to date with master and ready to issue a PR if you are.
