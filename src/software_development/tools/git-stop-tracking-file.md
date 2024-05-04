# git - Stop tracking a file

To stop tracking a file in git, you can use the following command:

```
git rm --cached <file>
```

**WARNING: While this will not remove the physical file from your local machine, it will remove the files from other developers' machines on their next `git pull`.**
