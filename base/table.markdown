# TABLE

##DDL语句 
>DDL[DATA DEFINITION LANGUAGE].


* create table
```sql 
	CREATE TABLE tablename
```

* show table column
```sql 
	DESC tablemane;
```

*  show table detail
```sql
	SHOW CREATE TABLE tablemane \g;
```

* delet table
```sql
	DROP TABLE tablemane;
```

* modify column
```sql
	ALTER TABLE tablename MODIFY [COLUMN] column_definition [FIRST|AFTER col_name]; 
```

* add column
```sql
	ALTER TABLE tablename ADD [COLUMN] column_definition [FIRST|AFTER col_name];
```

* del column
```sql 
	ALTER TABLE tablemane DROP [COLUMN] col_name;
```

* change colunm name 
```sql
	ALTER TABLE tablemane CHANGE [COLUMN] old_col_name column_definition[FIRST|AFTER col_name];
```

* change table name
```sql
	ALTER TABLE tablemane RENAME[TO]new_tablename;
```	

#####注意:
* column_definition = column_name column_val;


