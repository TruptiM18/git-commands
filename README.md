# day to day git-commands

To learn various git commands for version control.

GIT documentation available at https://git-scm.com/docs has been used to learn and take short note for following GIT commands.


1.
git-init - Create an empty Git repository or reinitialize an existing one
$ git init
Initialized empty Git repository in C:/Users/XXXX/Documents/git-commands/.git/

Running git init in an existing repository is safe. 
It will not overwrite things that are already there. 
The primary reason for rerunning git init is to pick up newly added templates (or to move the repository to another place if --separate-git-dir is given).

2.
git remote add origin - adds link to remote repository
$ git remote add origin https://github.com/TruptiM18/git-commands.git


3.
git pull - Incorporates changes from a remote repository into the current branch.
More precisely, git pull runs git fetch with the given parameters and calls git merge to merge the retrieved branch heads into the current branch. With --rebase, it runs git rebase instead of git merge.

$ git pull origin master
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/TruptiM18/git-commands
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master

4. 
git status - Tells you which files are edited/added/deleted and hence need to be added to be to index to commit.

$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

5.
git add -This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit.
It typically adds the current content of existing paths as a whole, but with some options it can also be used to add content with only part of the changes made to the working tree files applied, or remove paths that do not exist in the working tree anymore.
The "index" holds a snapshot of the content of the working tree, and it is this snapshot that is taken as the contents of the next commit. Thus after making any changes to the working tree, and before running the commit command, you must use the add command to add any new or modified files to the index.
$ git add README.md


6.
git push - Update remote refs along with associated objects
$ git push origin master
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 1.62 KiB | 829.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/TruptiM18/git-commands.git
   eaee12f..5e4a8b9  master -> master



