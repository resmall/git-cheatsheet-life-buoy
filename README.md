Git Cheat Sheet Situations
====================================

###What's this about

This cheatsheet purpose, is for my own reference, but feel free to fork, star etc... Tha main difference here is that this cheat sheet will be organized based on situations a user may encounter, as for instance:

<hr>
###How to undo a `git add`, or the opposite of git add. Both methods will result in the same.
```
git reset
git reset HEAD
```

###How to add a GitHub repository to your local repository so you can push it up
```
git remote add origin https://github.com/username/repo-name.git
```

###How to push the repository to GitHub
After adding the remote repository...
```
git push origin master
```

###GitHub still shows the deleted files in the repository, how to delete them [(Source)](http://stackoverflow.com/questions/6004453/how-to-remove-multiple-deleted-files-in-git-repository)
When you delete files locally and commit the change and push to the server, the shows this when you `git status`:
```
# On branch master
# Changes not staged for commit:
#   (use "git add/rm <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#   deleted:    public/components/file1.php
#   deleted:    public/components/file2.php
```

The safest way would be:
```
git rm public/components/file1.php \ 
       public/components/file1.php 
```

###I used `git rm -r`, how to undo this? [(Source)](http://stackoverflow.com/questions/2125710/how-to-revert-a-git-rm-r)
Just as you would do with a uncommited `git add`.
```
git reset HEAD
```

