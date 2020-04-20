# 添加和删除软连接
```
ln -s TARGET LINK_NAME
unlink LINK_NAME
```

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

#以xargs执行多条命令
cat foo.txt
one
two
three

cat foo.txt | xargs -I % sh -c 'echo %; mkdir %'
one 
two
three

ls 
one two three

#-t选项会把将要执行的命令显示于终端
echo 'one two three' | xargs -t rm
rm one two three

#-p选项会在执行命令之前提示用户进行确认
echo 'one two three' | xargs -p touch
touch one two three ?...
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
