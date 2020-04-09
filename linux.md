# xargs
```
#创建三个文件夹one two three
echo 'one two three' | xargs mkdir
#找出旧于14天以上的文件并删除
find /tmp -mtime +14 | xargs rm
#xargs v exec
#以下命令的作用相同
find ./foo -type -f -name "*.txt" -exec rm {} \;
find ./foo -type -f -name "*.txt" | xargs rm
#以查找和删除1000个文件为例，看谁的效率高
time find . -type f -name "*.txt" -exec rm {} \;
0.35s user 0.11s system 99% cpu 0.467 total

time find ./foo -type f -name "*.txt" | xargs rm
0.00s user 0.01s system 75% cpu 0.016 total
#实践证明，xargs 比 exec {} 快5倍。
```

# ps
```
#Check how long a process is up and running
ps -p <PID> -o lstart
```
# PSFTP.exe
```
CD /D "D:\PuTTY"
echo y | psftp.exe -v acct@ip -P 22 -i C:\Users\acct\ssh\xxxx.ppk -b D:\your_path\config.txt
```

# sftp
```
sftp -oIdentityFile=~/.ssh/id_isa -oPort=22 acct@ip
sftp -oIdentityFile=~/.ssh/id_isa -oPort=22 acct@hostname
```
