# Git

## Repository

- **Initialize repository**
    1. `mkdir /Uses/user/my_project`
    2. `git init`

- **Clone repository**  
  
    1. `git clone git@github.com:WilsonPan/cli-record.git`
    2. `git clone git@github.com:WilsonPan/cli-record.git --depth 1`
    3. `git clone git@github.com:WilsonPan/cli-record.git --branch master`

- **Change repository config**

    > Currently repository  

    1. `git config user.name "Wilson Pan"`
    2. `git config user.email johndoe@example.com`

    > Global

    1. `git config --global user.name "Wilson Pan"`
    2. `git config --global user.email johndoe@example.com`

## Branch

- **Create branch**

`git checkout -b feature-xxx`

- **Delete branch**
  
`git branch -d feature-xxx`

- **Pull Branch**
  
    1. `git pull`
    2. `git pull --rebase` -- working workspace clean

- **Merget multiple commit**
  
    1. `git rebase -i Head~n`
    2. change commit history
    3. change commit message
    4. git push

## Version control

- **Stage file**
    1. `git add .` -- for all (added  && modified  && deleted) 
    2. `git add -u` -- for tracked files
    3. `git add *.md` -- for all *.md files
    4. `git add git*` -- for name start with git
    5. `git stage` -- synonym for git add

- **Commit changes**
    1. `git commit`
    2. `git commit -m 'commit message'`

- **Restore commit**

  - Not published

    1. `git reset <id>`
    2. `git reset HEAD^3` -- reset last 3 commits

  - Published

   1. `git revert <id>`

- **Merge other branch**
    1. `git merge <branch_name>`            -- merge everything
    2. `git merge --squash <branch_name>`   -- create new commit , not commit

- **Logs**
    1. `git log`
    2. `git log --oneline`
    3. `git log --oneline -n 10`

- **Diff**
    1. `git diff` -- (current workspace) vs (commited & staged)
    2. `git diff --stat` -- simple diff result
    3. `git difff <id1> <id2>` -- for commit differences
    4. `git diff <branch1> <branch2>` -- for branch differences
    5. `git diff test` -- for current workspace differences with branch 'test'

- **Clean commit message**
    1. `git checkout --orphan <branch_name>`  -- **create a new orphan branch**
    2. `git add . && git commit -m 'commit message'`
    3. `git branch -d master`
    4. `git branch -m master`
    5. `git push -f origin master` -- **force push to origin branch**
