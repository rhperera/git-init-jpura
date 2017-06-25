Keeps track of changes, specially in text files
Manages vesrion of files (A VCS)
Programmers use this for Source Code Management (SCM)
Could based vcs will save your day
Working with a team

What would you do
file_v1.txt file_v2.txt etc.
Undoing or rollback changes

git help <command>

git init - track all changes in this directory

Git configurations
System level - etc/gitconfig or Program Files/Git/etc/gitconfig - git config --system
User level (Global) - ~/.gitconfig or $HOME/.gitconfig - git config --global
Project level (Local) - [project-folder]/.git/gitconfig - git config --local

git config --global core.editor "atom.exe -wl1"
git config --global color.ui true

Make a change.
git add . or git add --all
git commit -m "the message"

writing meaningful commit messages
write in present tense
short but descriptive
[filetypes], bugfix:, #ticket_number-

add a .gitkeep file to add directories for tracking
git only tracks files

git log
----------
git log -n <numberof-commits-toshow>
git log --since=yyyy-mm-dd
git log --until=yyyy-mm-dd
git log --author="name"
git log --grep="init"

git diff
---------
git diff [commithash] [filename] (diff with repository)
git diff --staged (diff with the staging)

git ignore
-----------
git config --global core.excludesfile <path>
git config --local core.excludesfile <path>

git rm --cached filename (remove from staging)

Delete Files
--------------
Delete the staged file
git rm <filename> - deletes the file from staging area

Easy thing
git rm <filename> (This will not put the file in trash. it will delete forever)

delete all unstaged
git clean -n (warning about the files to remove)
git clean -f (force)

Rename
--------
git add <newfilename>
git rm <oldfilename>
or
git mv <old> <new>


git show
--------------
https://git-scm.com/docs/git-show


git status

git checkout
----------------
git checkout -- <filename>

git reset
----------------
git reset HEAD <filename> (unstage the file)
git reset --soft <hash> (change head pointer of repo only)
git reset --mixed <hash> ()
git reset --hard <hash> (change all. all uncommited changes are lost)


git commit --ammend
---------------
first add to staging
git commit --ammend -m <message>

retrieve old commit
git checkout <commithash> -- <filename>

git revert
---------------
git revert <hash>


git branch
------------
git branch
git branch <branchname> (creates a branch)
git checkout <branchname>
git checkout -b <branchname> (do both at once)

git branch --move <oldtitle> <newtitle>
git branch --delete <branch>

git merge
-------------
git merge <branch-tomerge-from> (-> git merge --abort)

git stash
-------------
git stash save <message>
git stash list
git stash show -p stash@{0} (show as patch)
git stash pop (add and remove)
git stash apply
git stash drop stash@{0}

compare branches
------------------
git diff <branch1>..<branch2>
git branch --merged

git remotes
--------------
git remote
git push
git pull
git fetch
git remote add <alias> <URL>
git branch --set-upstream <branch> <alias/branch>
git push -u <alias> <branch> (track this remote branch)
