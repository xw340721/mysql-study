# TABLE

##DDL语句 
>DDL[Data Definition Language].


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




##DML语句
>DML语句[Data Mainpulation Language].

* insert data
```sql
	INSERT INTO tablemane (field1,field2,...,fildn) VALUE(value11,value12,...,value1n),
														 (value21,value22,...,value2n);
```
* update data
```sql
	UPDATE tablename SET field1=value1,field2=value2,...,fieldn=valuen [WHERE CONDITION];
	//or
	UPDATE tb1,tb2,...,tbn set tb1.field1=expr1,tbn.fieldn = exprn [WHERE CONDITION];//page 35
```	 

* delet data
```sql
	DELETE FORM tablemane [WHERE CONDITION];
	//or
	DELETE t1,t2,...,tn from t1,t2,...tn [WHERE CONDITION];//如果form为表别名 from前面也要换成别名;
```

* search data 
```sql
	SELECT * FROM tablename [WHERE CONDITION];
	//eg1 去除重复记录
	SELECT DISTINCT column_name from tablename;
	//limit ordre
	SELECT * FROM tablemane [WHERE CONDITION] [ORDER BY field1 [DESC|ASC]],[ORDER BY field2 [DESC|ASC]],...,[ORDER BY fieldn [DESC|ASC]];
	SELECT * FROM tablemane [LIMIT offset_start,row_count]; 
	//聚合
	SELECT [field1,field2,...,fieldn] fun_name FROM tablemane [WHERE where_condition] [GROUP BY 
	field1,field2,...,fieldn] [WITH ROLLUP] [HAVING where_condition];
	//内联
	SELECT field1,field2,...,fieldn from tb1,tb2,...,tbn [WHERE CONDITION];
	//外联
	SELECT field1,field2 from tb1 left join tb2 on tb1.field1=tb2.field1 [WHERE CONDITION];
	SELECT field1,field2 from tb1 right join tb2 on tb1.field1=tb2.field1 [WHERE CONDITION];
	//子查询
	SELECT field1,field2,...,fieldn from tb1 WHERE field1 IN (select field1 from tb2 );
	SELECT field1,field2,...,fieldn from tb1 WHERE field1 = (select field1 from tb2 limit 1 );
	//联合查询
	SELECT field1 from tb1 UNION ALL select field1 from tb2;
	SELECT field1 from tb1 UNION select field1 from tb2;
```	


#####注意:
* column_definition = column_name column_val.
* fun_name 为聚合函数 sum count max min,会产生一列数据.
* count(1) 表示统计全部,count(column_name)表示该字段进行统计.
* HAVING 为分类后继续条件过滤,必须在grouup by .
* with  rollup 为统计总共人数.
* 内联外联区别:
	*内联货匹配俩张表中相互的记录.
	*外联会匹配其他不能匹配的记录. 
* UNICON 和 UNICON ALl 区别在于UNICON 会把UNICON ALL 进行一次DISTINCT

##DLC语句
>DLC语句[Data Control Language]

