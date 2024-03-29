# [go back to Overview](https://github.com/c4arl0s)

# [Summary-git-commands](https://github.com/c4arl0s/Summary-git-commands#go-back-to-overview)

1. [Quick Reference](https://github.com/c4arl0s/Summary-git-commands#1-quick-reference-tap-to-see-topic)
2. [Quick Reference - The Basics](https://github.com/c4arl0s/Summary-git-commands#2-quick-reference---the-basics-tap-to-see-complete-topic)
3. [Quick Reference - Undoing Changes](https://github.com/c4arl0s/Summary-git-commands#3-quick-reference---undoing-changes-tap-to-see-complete-topic)
4. [Quick Reference - Branches I](https://github.com/c4arl0s/Summary-git-commands#4-quick-reference---branches-i-tap-to-see-topic)
5. [Quick Reference - Branches II](https://github.com/c4arl0s/Summary-git-commands#5-quick-reference---branches-ii-click-to-see-topic)
6. [Quick Reference - Rebasing](https://github.com/c4arl0s/Summary-git-commands#6-quick-reference---rebasing-tap-to-see-topic)
7. [Quick Reference - Rewriting History](https://github.com/c4arl0s/Summary-git-commands#7-quick-reference-tap-to-see-topic)
8. [Quick Reference - Remotes](https://github.com/c4arl0s/Summary-git-commands#8-quick-reference---remotes-tap-to-see-topic)
9. [Quick Reference - Centralized Workflows](https://github.com/c4arl0s/Summary-git-commands#9-quick-reference---centralized-workflows-tap-to-see-topic)
10. [Quick Reference - Distributed Workflows](https://github.com/c4arl0s/Summary-git-commands#10-quick-reference---distributed-workflows-tap-to-see-topic)
11. [Quick Reference - Patch Workflows](https://github.com/c4arl0s/Summary-git-commands#11-quick-reference---patch-workflows-tap-to-see-topic)
12. [Quick Reference - Tips and Tricks](https://github.com/c4arl0s/Summary-git-commands#12-quick-reference---tips-and-tricks-tap-to-see-topic)
13. [Quick Reference - Plumbing](https://github.com/c4arl0s/Summary-git-commands#13-quick-reference---plumbing-tap-to-see-topic)
14. [Rename a branch](https://github.com/c4arl0s/Summary-git-commands#14-rename-a-branch)
15. [Merging 2 git reporsitories into One, keeping history](https://github.com/c4arl0s/Summary-git-commands#15-merging-2-git-reporsitories-into-one-keeping-history)
16. [Reset only one file](https://github.com/c4arl0s/Summary-git-commands#16-reset-only-one-file)
17. [Set mergetool](https://github.com/c4arl0s/Summary-git-commands#17-set-mergetool)
18. [Use vimdiff to solve conflicts](https://github.com/c4arl0s/Summary-git-commands#18-use-vimdiff-to-solve-conflicts)
19. [Update Github token](https://github.com/c4arl0s/Summary-git-commands#19-update-github-token)
20. [Create a remote repository from a local repository using gh command](https://github.com/c4arl0s/Summary-git-commands#20-create-a-remote-repository-from-a-local-repository-using-gh-command)
21. [Add a repository inside a repository](https://github.com/c4arl0s/Summary-git-commands#21-add-a-repository-inside-a-repository)

# [1. Quick Reference](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
git config --global user.name "c4arl0s"
```

```console
git config --global user.email c.santiago.cruz@example.com
```

```console
git config --global core.editor vim
```

```console
touch ~/.git-message.txt; echo "subject line" > ~/.git-message.txt; echo "What happened" >> ~/.git-message.txt;
```

```console
git config --global commit.template ~/.git-message.txt
```

```console
echo "*~" > ~/.gitignore_global; echo ".DS_Store" >> ~/.gitignore_global
```

```console
git config --global core.excludesfile ~/.gitignore_global
```

# [2. Quick Reference - The Basics](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see Complete topic](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
git init
```

Create a git repository in the current folder.

```console
git status
```

View the status of each file in a repository.

```console
git add fileName
```

Stage a file for the next commit.

```console
git commit
```

Commit the staged files with a descriptive message.

```console
git log
```

View a repository's commit history.

```console
git config --global user.name "<nameOfTheUser>"
```

Define the author name to be used in all repositories.

```console
git config --global user.email <email>
```

Define the author email to be used in all repositories.


# [3. Quick Reference - Undoing Changes](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see Complete topic](https://github.com/c4arl0s/3UndoingChangesRysGitTutorial#3-undoing-changes-rys-git-tutorial---content)


```console
git checkout commitID
```
View a previous commit.

```console
git tag -a tagName -m "description"
```
Create an annotated tag pointing to the most recent commit.

```console
git revert commitID
```
Undo the specified commit by applying a new commit.

```console
git reset --hard
```
Reset tracked files to match the most recent commit.

```console
git clean -f
```
Remove untracked files.

```console
git reset --hard / git clean -f
```
Permanently undo uncommitted changes.

# [4. Quick Reference - Branches I](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/4BranchesIRysGitTutorial#4-branches-i-rys-git-tutorial---content)

```console
git branch
```

List all branches.

```console
git branch <branchName>
```

Create a new branch using the current working directory as its base.

```console
git checkout <branchName>
```

Make the working directory and the HEAD match the specified branch.

```console
git merge <branchName>
```

Merge a branch into the checked-out branch.

```console
git branch -d <branchName>
```

Delete branchName

```console
git rm <fileName>
```

Remove a file from the working directory (if applicable) and stop tracking the file.

```console
git push origin --delete <remote-branch-to-remove>
```

This flag allows you to delete a remote branch. (--delete)

# [5. Quick Reference - Branches II](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Click to see topic](https://github.com/c4arl0s/5BranchesIIRysGitTutorial#5-branches-ii---content)

```console
git commit -a -m "messageToCommit"
```

Stage all tracked files and commit the snapshot using the specified message.

```console
git branch -D branchName
```

Force the removal of an unmerged branch (be careful: it will be lost forever).

# [6. Quick Reference - Rebasing](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/6RebasingRysGitTutorial#6-rebasing---content)

```console
git rebase newBase
```
Move the current branch's commits to the tip of new-base, which can be either a branch name or a commit ID.

```console
git rebase -i newBase
```
Perform an interactive rebase and select actions for each commit.

```console
git commit --amend
```
Add staged changes to the most recent commit instead of creating a new one.

```console
git rebase --continue
```
Continue a rebase after amending a commit.

```console
git rebase abort
```
Abandon the current interactive rebase and return the repository to its former state.

```console
git merge --no-ff branchName
```
Force a merge commit even if Git could do a fast-forward merge.

# [7. Quick Reference - Rewriting History](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/6Rebasing#6-rebasing---content)

In this case that I am going to document I found that I wanted to commit in my history a commit which contains a work that I didn't want to lose. So first, I tried to rebase main with  C1 and C2, but C1 had merge conflicts with the last commit on main branch.

![51265589-0703-4327-BDA7-7696793FD67F-1-2048x1536-0-oriented copy](https://user-images.githubusercontent.com/24994818/115579497-d86b5a00-a28b-11eb-9d92-daf464eba648.png)

This branch was not essential for the project because the idea was too complex, so I just wanted to commit the executed work. So in order to commit this work you have to squash C1 and C2 in one commit. You can do this doing an interactive rebase.

Solution 1:

- Remove last commit (it has minimum changes on main branch)
- Then try to do the interactive rebase. 
- Once you rebase the main branch you are able to marge this branch.
- After merging, you are able to revert this commit, which contains the "executed work" and keep it in the history.

The interactive rebase was successful, because it is a fast forward. In this case last commit had minimum changes so I was able to discard them.

Solution 2:

- In order to keep "last commit". You have to rebase your branch with minimum number of commits, I mean one commit. So then try to do the rebase. 
- Once you are able to do the rebase, you merge this branch and then revert this commit, remember, this commit it is juts to insert this effort in the history line.

# [git squash older commits (not last one)](https://github.com/c4arl0s/6Rebasing#6-rebasing---content)

1. Start an interactive rebase:

```console
git rebase -i HEAD~n
```

> n: is how far do you want to go back in history

2. Your default text editor will open. At the top, a list of your latest `n` commits will be displayed, in reverse order.

```console
pick a5f4a0d commit-1
pick 19aab46 commit-2
pick 1733ea4 commit-3
pick 827a099 commit-4
pick 10c3f38 commit-5
pick d32d526 commit-6
```

3. replace `pick` keyword with `squash` keyword in order to try to squash those commits:

```console
pick a5f4a0d commit-1
squash 19aab46 commit-2
squash 1733ea4 commit-3
squash 827a099 commit-4
squash 10c3f38 commit-5
pick d32d526 commit-6
```

4. Save and exit.

5. Git will apply all changes and will open again your editor to merge the three commit messages. You can modify your commit messages or leave it as it is (if so, the commit messages of all commits will be concatenated).

# [7. Quick Reference](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/7RewritingHistoryRysGitTutorial#7-rewriting-history-rys-git-tutorial---content)

```console
git reflog
```

```console
git reset --mixed HEAD~n
```
Move the HEAD backward n commits, but do not change the working directory

```console
git reset --hard HEAD~n
```

Move the HEAD backward n commits, and change the working directory to match.

```console
git log since..until
```
Display the commits reachable from until but not from since. These parameters can be either commit ID's o branch names.

```console
git log --stat
```
Include extra information about altered files in the log output.

# [Own Experiences](https://github.com/c4arl0s/7RewritingHistory#own-experiences-using)

# [Revive the lost commit](https://github.com/c4arl0s/7RewritingHistory#own-experiences-using)

I used to do `git reset HEAD~` to include insignificant changes in the last commit. But after including those changes, I did included important changes. These important changes were not good, so I was losing my functional version of the project. To revive the commit you have to do this:

1. `git reflog`
2. Look for the commit you remember have the functional version.
3. go to the commit with the functional version: `git checkout <commitWithFuncionalVersion>`
4. Then: `git checkout -b functionalBranch`
5. Now: go back to the main branch: `git checkout main`.
6. Finally merge the functional branch: `git merge functionalBrancg`
7. Remember: with git you don't miss any information.

# [8. Quick Reference - Remotes](https://github.com/c4arl0s/8RemotesRysGitTutorial#8-remotes-rys-git-tutorial---content) [Tap to see topic]()

```console
git clone <remotePath>
```
Create a copy of a remote Git repository

```console
git remote
```
List remote repositories.


```console
git remote add <remoteName> <remotePath>
```
Add a remote repository


```console
git fetch <remoteName>
```
Download remote branch information, but do not merge anything

```console
git merge <remoteName>/<branchName>
```
Merge a remote branch into the checked-out branch

```console
git branch -r
```
List remote branches

```console
git push <remoteName> <branchName>
```
Push a local branch to another repository

```console
git branch -r
```
List remote branches.

```console
git push <remoteName> <branchName>
```
Push a local branch to another repository

```console
git push <remoteName> <tagName>
```
Push a tag to another repository

# [Use an old repository to push the current branch to another repository in Github](https://github.com/c4arl0s/8RemotesRysGitTutorial#8-remotes-rys-git-tutorial---content)

1. Create a repository on github, name: RepositoryOnGithub
2. Navigate to the original repository you want to use

```console
cd /path/to/original/repository
```

2. Push the master or main branch, force to delete the trash you create after creating it.

```console
git push -f https://github.com/c4arl0s/RepositoryOnGithub.git master:main
```

3. Clone RepositoryOnGithub repository. It will contain all the files and history of the original repository.

```console
git clone https://github.com/c4arl0s/RepositoryOnGithub.git
```

# [9. Quick Reference - Centralized Workflows](https://github.com/c4arl0s/9CentralizedWorkflowsRysGitTutorial#9-centralized-workflows-rysgit-tutorial---content) [Tap to see topic]()

```console
git init --bare <repositoryName>
```
Create a Git repository, but omit the working directory

```console
git remote rm <remoteName>
```
Remove the specified remote from your book-marked connections.

# [10. Quick Reference - Distributed Workflows](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/11PatchWorkflowsRysGitTutorial#11-patch-workflows---content)

# [11. Quick Reference - Patch Workflows](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/11PatchWorkflowsRysGitTutorial#11-patch-workflows---content)

```console
git format-patch branchName
```
Create a patch for each commit contained in the current branch but not in branchName. You can also specify a commit ID instead of branchName

```console
git am < patchFile
```
Apply a patch to the current branch

# [12. Quick Reference - Tips and Tricks](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/12TipsAndTricksRysGitTutorial#12-tips-and-tricks---content)

```console
git archive branchName --format=zip --output=fileName
```
Export a single snapshot to a ZIP archive called fileName

```console
git bundle create fileNam branchName
```
Export an entire branch, complete with history, to  the specified fileName

```console
git clone repo.bundle repoDirectory -b branchName
```
Re-create a project from a bundle repository and checkout branchName

```console
git stash
```
Temporarily stash change to create a clean working directory

```console
git stash apply
```
Re-apply stashed changes to the working directory

```console
git diff commitID..anotherCommitID
```
View the difference between two commits

```console
git diff
```
View the difference between the working directory and the stagging area.

```console
git reset HEAD fileName
```
Unstage a file, but don't alter the working directory or move the current branch

```console
git checkout commitID fileName
```
Revert and individual file to match the specified commit without switching branches

```console
git config --global alias.aliasName gitCommand
```
Create a shortcut for a command and store it in the global configuration file

<<<<<<< Updated upstream

# [How to create a global gitignore file](https://github.com/c4arl0s/12TipsAndTricksRysGitTutorial#12-tips-and-tricks---content)

```console
echo .DS_Store >> ~/.gitignore_global
```

then:

```console
git config --global core.excludesfile ~/.gitignore_global
```

Now each commit you will not be able to add any `.DS_Store` file.

> If you already add a .DS_Store file in your repo, you have to delete it manually.

# [How to create a pull request from your local branch](https://github.com/c4arl0s/12TipsAndTricksRysGitTutorial#12-tips-and-tricks---content)

You can create a pull request on your own project just pushing your branch

Console output:

```console
git push origin <nameOfTheBranch>
```

Then on Github will appear the message that you can generate a pull request, follow the instructions and ask for the pull request, someone in the project then can merge your branch on main or develop branch.

![Screen Shot 2021-09-13 at 8 29 38](https://user-images.githubusercontent.com/24994818/133092868-8b28bb21-c6db-4c63-814e-d5b87b491bc6.png)
![Screen Shot 2021-09-13 at 8 30 18](https://user-images.githubusercontent.com/24994818/133092874-1479c0dd-36d4-43a9-9465-ab0300182240.png)
![Screen Shot 2021-09-13 at 8 30 45](https://user-images.githubusercontent.com/24994818/133092883-550a225f-a5fa-401c-97cc-0839b947854f.png)
![Screen Shot 2021-09-13 at 8 31 29](https://user-images.githubusercontent.com/24994818/133092892-42fcfeef-d13e-481b-b1e9-4ced46694699.png)

# [How to fetch a branch from another team member and merge](https://github.com/c4arl0s/12TipsAndTricksRysGitTutorial#12-tips-and-tricks---content)


Once you did push (your buddy)  a branch to the repository, you can fetch the branch to your macbook with these commands:

1. Step 1: From your project repository, bring in the changes and test.

```console
git fetch origin
git checkout -b CSC/13-how-to-fetch-a-branch-and-merge-Only-Test origin/CSC/13-how-to-fetch-a-branch-and-merge
```

> In this case I had to create another branch with different name in order to test the branch that it is on `origin` (because I have not buddy :-( )

2. Step 2: Run a test, verify if everything is ok.

3. Step 3: Merge the changes and update on GitHub.

```console
git checkout master
git merge --no-ff CSC/13-how-to-fetch-a-branch-and-merge
```

4. Step 4: Push the current branch (master) to origin.

```console
git push origin master
```

# [Remove .DS_Store files recursively](https://github.com/c4arl0s/12TipsAndTricks#12-tips-and-tricks---content)

If you already created these `.DS_Store` files, use this command.

```console
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
```
Console output example:

```console
rm 'Projects/.DS_Store'
rm 'Projects/1ButtonsProjectCommonInputControls/.DS_Store'
rm 'Projects/2SwitchesProjectCommonInputControls/.DS_Store'
rm 'Projects/3SlidersProjectCommonInputControls/.DS_Store'
rm 'Projects/4TextFieldsProjectCommonInputControls/.DS_Store'
rm 'Projects/5ActionsAndOutletsProjectCommonInputControls/.DS_Store'
rm 'Projects/6GestureRecognizersProjectCommonInputControls/.DS_Store'
rm 'Projects/7ProgrammaticActionsProjectCommonInputControls/.DS_Store'
rm 'Projects/LabStep1CreateYourViewInInterfaceBuilderTwoButtons/.DS_Store'
rm 'Projects/LabStep2CreateOutletsAndActionsTwoButtons/.DS_Store'
rm 'Projects/LabStep3AddCodeForYourActionsTwoButtons/.DS_Store'
```

# [13. Quick Reference - Plumbing](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands) [Tap to see topic](https://github.com/c4arl0s/13PlumbingRysGitTutorial#13-plumbing---content)
 
```console
git cat-file type objectID
```
Display the specified object, where type is one of commit, tree, blob, or tag.

```console
git cat-file -t objectID
```
Output the type of the specified object.

```console
git ls-tree treeID
```
Display a pretty version of the specified tree objects.


```console
git gc
```
Perform a garbage collection on the object database.

```console
git update-index --add file
```
Stage the specified file, using the optional --add flag to denote a new untracked file.

```console
git write-tree
```
Generate a tree from the index and store it in the object data-base. Returns the ID of the new tree object.

```console
git commit-tree treeID -p parentID
```
Create a New commit object from the given tree object and parent commit. Returns the ID of the new commit object.

# [14. Rename a branch](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

Console output:

```console
git branch -m old-name-branch new-name-branch
```

Rename a branch

# [15. Merging 2 git reporsitories into One, keeping history](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

1. Create a Merge-2-Unrelated-Projects directory
2. Inside Merge-2-Unrelated-Projects clone both repostories, Example: trad3 and DictEnEsScript
3. Change to trad3 directory repository (4 years old).
4. Type this command:

```console
filter-branch --index-filter \ 
'git ls-files -s | sed "s-control+v, TAB\"-&trad3/-" |
GIT_INDEX_FILE=$GIT_INDEX_FILE.new \
git update-index --index-info && 
mv "$GIT_INDEX_FILE.new" "$GIT_INDEX_FILE"' HEAD
```

> Remember the line where it says `trad3`

5. Create a new repo, where first and second project are located, in this case I will call it DictEnEs (shorter)

```console
mkdir DictEnEs
```

Then: 

```console
cd DictEnEs; git init
```

4. Add the 2 repos as remote repos for the new "DictEnEs" 

```console
git remote add --fetch trad3 ../trad3
git remote add --fetch 
DictEnEsScript ../DictEnEsScript
```

5. Merge the 2 remote repos

```console
git merge trad3/master --allow-unrelated-histories
```

6. Take a look and see that the log is present:

```console
git log
```

7. Move these new files into a new directory to avoid conflicts, `mkdir OldTrad3Repository` and move all files.
8. Create a new commit with these new files

```console
git add .; git commit -m "add files that comes from old trad3 repository"
```

9. Now merge the files that come from the second repository

```console
git merge DictEnEsScript/master --allow-unrelated-histories
```

As you can see the merge is successfully. WoW!.

Thank you to [Medhat Dawoud Tutorial](https://medhatdawoud.net/blog/merging-2-git-repos-with-persisting-commit-history)

# [16. Reset only one file](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

```console
git restore fineName
```

# [17. Set mergetool](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

```console
git config --global merge.tool vimdiff
```

# [18. Use vimdiff to solve conflicts](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

1. After executing the command merge, lets say that you are working on a branch and it is needed to merge new updates to your work:

```console
git merge main
```

2. Your console is going to say that there is merge conflics, then you invoke vimdiff as:

```console
git mergetool --tool=vimdiff
```

3. Once you finish editing all the files that contains conflicts, save and create a new commit.

4. Make sure that all is up to date.

# [19. Update Github token](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

<img width="219" alt="Screen Shot 2022-03-11 at 6 19 52 a m" src="https://user-images.githubusercontent.com/24994818/157866481-beaf64ab-0f14-43f9-b1f1-234ee1d0608e.png">
<img width="222" alt="Screen Shot 2022-03-11 at 6 20 07 a m" src="https://user-images.githubusercontent.com/24994818/157866497-abfad782-48d6-42e7-a3fe-d18a3b7142d5.png">
<img width="300" alt="Screen Shot 2022-03-11 at 6 20 18 a m" src="https://user-images.githubusercontent.com/24994818/157866506-8e67a77a-5dcd-4b25-81a3-11b736cb2773.png">
<img width="318" alt="Screen Shot 2022-03-11 at 6 20 45 a m" src="https://user-images.githubusercontent.com/24994818/157866516-7d968f92-6448-4a0b-ae48-aef94b6b0b09.png">

If you lost the current tokens, create a new one, and update your repository access.

# [20. Create a remote repository from a local repository using gh command](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

1. Authenticate if necessary: `gh auth login`
2. Start using git: `git init`
3. Create repository: `gh repo create`

# [21. Add a repository inside a repository](https://github.com/c4arl0s/Summary-git-commands#summary-git-commands)

```console
git submodule add git@github.com:c4arl0s/5iOSApplicationDevelopment.git
```

