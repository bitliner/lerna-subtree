# lerna-subtree
Manage lerna with git subtree

# Proposal

A list of commands to help manage lerna sub-projects with git subtree.

Commands:

- **lerna-subtree add <GIT_REMOTE_URL> <branch>**

  1. it runs command `git remote add <REPO_NAME> <GIT_REMOTE_URL>` if remote does not exist
  2. it runs `git subtree add --prefix=packages/<REPO_NAME> <REPO_NAME> <branch>`
 
- **lerna-subtree publish**

  1. it runs `lerna publish`
  2. it runs, for each sub-tree, `git subtree --prefix=packages/<REPO_NAME> push <REPO_NAME> --all`
