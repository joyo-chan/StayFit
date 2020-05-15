# Search branch name and its parent name
```
select comcode, upcomcode, name
  from tableA
 start with comcode = '00'
 connect by upcomcode = prior comcode
```
查询结果
| COMCODE|UPCOMCODE |NAME |
|----|----|----|
| 00| |xxx |
| 1521|00|xxx |
| 152101|1521|xxx |
| 152102|1521|xxx |



# How to retrieve the current value of an oracle sequence without increment it?
```
SELECT ERRMSG_SEQ.nextval FROM DUAL;
SELECT ERRMSG_SEQ.currval FROM DUAL;  --273085
select last_number from user_sequences where sequence_name='ERRMSG_SEQ';  --273662
```
[stackoverflow](https://stackoverflow.com/questions/10210273/how-to-retrieve-the-current-value-of-an-oracle-sequence-without-increment-it)


#
```
```
