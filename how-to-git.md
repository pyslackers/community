# How to Use git When Contributing to Our Projects

The goal is to fork and preserve the state of the project at the time that you forked it, while contributing development branches to the original/upstream project.

Keeping your forked/master in tact allows others to more easily work with your forked copy.

Here are the steps with links to documentation:

1. [Fork to your GitHub account](https://help.github.com/articles/fork-a-repo/#fork-an-example-repository)
1. [Clone your forked copy onto your computer](https://help.github.com/articles/fork-a-repo/#step-2-create-a-local-clone-of-your-fork)
1. [Set master project repo as the upstream for your cloned repo](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
1. Create a new branch **(don't develop on 'Master')**
    > git checkout -b <new-branch-name>
1. Develop (remember to save often ;) )
1. Commit to your development branch
    > git commit -m "Briefly explain your contribution"
1. Sync your copy with latest upstream copy (in case the project changed while you were developing)
    > * git fetch upstream
    > * git checkout master
    > * git merge upstream/master
    
    > If upstream/master has new commits:
    > * git checkout <new-branch-name>
    > * git rebase master (resolve conflicts, if any)
1. Push your new branch to your forked repo
    > git push origin <new-branch-name>
1. [Create PR from GitHub w/out merging to your master](https://help.github.com/articles/creating-a-pull-request-from-a-fork/)

## Git Resources
If you are new to git, read [the book](https://www.git-scm.com/book/en/v2)

[Reference Manual](https://www.git-scm.com/docs)

[A very nice explanation of a typical fork and PR workflow](https://gist.github.com/Chaser324/ce0505fbed06b947d962)