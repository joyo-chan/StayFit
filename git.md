## deleting a local branch with git

Switch to some other branch and delete Test_Branch, as follows:
```
$ git checkout master
$ git branch -d Test_Branch
```
If above command gives you error - The branch 'Test_Branch' is not fully merged. If you are sure you want to delete it and still you want 
to delete it, then you can **force delete it** using -D instead of -d, as:
```
$ git branch -D Test_Branch
```
To delete Test_Branch from remote as well, execute:
```
git push origin --delete Test_Branch
```

****
```
```

