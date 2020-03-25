# How to retrieve the current value of an oracle sequence without increment it?
```
#https://stackoverflow.com/questions/10210273/how-to-retrieve-the-current-value-of-an-oracle-sequence-without-increment-it
SELECT ERRMSG_SEQ.nextval FROM DUAL;
SELECT ERRMSG_SEQ.currval FROM DUAL;  --273085
select last_number from user_sequences where sequence_name='ERRMSG_SEQ';  --273662
```

****
```
```
