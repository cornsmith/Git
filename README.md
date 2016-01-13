# Git cheatsheet

#### Setting up
```sh
git config --global user.name "User Name"
git config --global user.email "email"
```

#### Creating
```sh
# create new local repo
git init

# adding a remote and verifying
git remote add origin https://github.com/username/repo.git
git remote -v

# clone existing repo to local
git clone http://github.com/username/repo.git local_name
```

#### Staging
```sh
# add file to stage
git add filename.ext

# add all files
git add -A

# check status of files (working directory and staging)
git status

# difference between working directory and staging
git diff

# discard changes
git checkout HEAD filename

# unstage file changes in staging
git reset HEAD filename

# reset to previous commit
git reset SHA
```

#### Committing
```sh
# commit
git commit -m "message"

# log of commits
git log
```

#### Fetching
```sh
# fetch from remote
git fetch

# merge origin/master into local branch
git merge origin/master

# push local branch to remote
git push origin branch_name

# list project's remotes
git remote -v
```

#### Branching and merging
```sh
# view all branches
git branch

# create new local branch
git branch new_branch

# switch to branch
git checkout branch_name

# delete a local merged branch
git branch -d branchname

# delete a local branch - WILL delete even if not merged yet
git branch -D branchname
```

#### Merging
```sh
# First checkout master
git checkout master

# Now merge branch to master
git merge branch_name

# To cancel a merge
git merge --abort
```

#### Syncing a fork
```sh
git fetch upstream
git checkout master
git merge upstream/master
```