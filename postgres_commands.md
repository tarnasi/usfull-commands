# Postgres Commands

- We start with how change the sequence of primary key of a table
### ${table}_${column}_seq
```
SELECT setval('"public"."constant_sensor_id_seq1"', 41, true);
```
- IF we don't know what problem is and it not working we dump table and in a sql file the ```seq``` is it.
