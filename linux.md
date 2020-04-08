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
