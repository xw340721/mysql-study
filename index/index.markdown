#索引设计和使用

## 创建索引

* create index
```sql 
	CREATE [UNIQUE|FULLTEXT|SPATIAL] INDEX index_name [USING index_type] on tb1_name(index_col_name,...);
	//
	index_col_name:
		col_name[(length)][ASC|DESC];
```	

* drop index
```sql
	DROP INDEX index_name on tb1_name;
```	