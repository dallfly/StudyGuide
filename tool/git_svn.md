# Git SVN
Use git for svn repository.

## Create svn repository by local git repository

### Create svn repository
``` bash
svn mkdir -m "create new project" http://path/NewProject http://path/NewProject/trunk http://path/NewProject/branches http://path/NewProject/tags
```

### Push git repository to svn repository
``` bash
cd /path/to/git/localrepo
git svn init http://path/NewProject -s
git reset --hard remotes/origin/trunk
git svn fetch
git svn rebase origin/trunk
git svn dcommit
```

## Git clone from svn repository
``` bash
git svn clone http://path/NewProjects -s
```

## Git SVN Commands

### Add a new commit in local git repository
* The commit is only stored in local repository.
``` bash
git commit
```
* Push local commit to svn repository
``` bash
git svn dcommit
```
