# git cheatsheet


|  Command  | Sample  | Description  |
| :-------- | :-----:  | -------: |
| git init  | - | Create new Repo in current directory |
| git clone | git clone https://github.com/octocat/Hello-World.git | Clone a remote repository |
| git branch -av | - | List all existing branches |
| git checkout --track [remote/branch] | git checkout --track origin/master |  Track the remote branch named feature-branch-foo |
| git branch -d [branch] | git branch -d master |  Delete local branch `master` |
| git push origin :[branch] | git push origin :master |  Delete remote branch `master` |
| git rebase -i [branch] | git rebase -i develop | Rebase your current HEAD onto [branch] |