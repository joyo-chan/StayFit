# EOF or read error
```
Archive:  uploaded.zip
replace OFD_03_960_20200529_02.TXT? [y]es, [n]o, [A]ll, [N]one, [r]ename:  NULL
(EOF or read error, treating as "[N]one" ...)
Build step 'Execute shell' marked build as failure

#解决办法
#-o  overwrite files WITHOUT prompting
unzip -o uploaded.zip
```





```
```
