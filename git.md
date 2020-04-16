
**How to delete a git branch both locally and remotely**
```
// delete branch locally
git branch -d localBranchName

// delete branch remotely
git push origin --delete remoteBranchName
```

## Linux查看某个进程的启动时间
```
ps -p <PID> -o lstart
```

## 放弃本地某个文件的修改，或所有修改
```
git checkout 文件名
git checkout #放弃所有文件的所有修改
git reset --hard 版本号 #返回到某个版本，放弃所有修改
git log
git log 文件名
git checkout <commit_id> file/folder/wildcard
#https://www.cnblogs.com/acm-bingzi/p/gitCheckout.html
```

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

