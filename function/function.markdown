#mysql 常用函数

## 字符串函数

* CONTACT(s1,s2,...,sn);
* INSERT(str,x,y,instr);
* LOWER(str);
* UPPER(str);
* LEFT(str,x);
* RIGHT(str,x);
* LPAD(str,n,pad);
* RPAD(str,n,pad);
* LTRIM(str);
* RTRIM(str);
* REPEAT(str,x);
* REPLACE(str,a,b);
* STRCMP(s1,s2);
* TRIM(str);
* SUBSTRING(str,x,y);

## 数值函数

* ABS(x);
* CEIL(x);//取出比x大的最小整数
* FLOOR(x);//取出比x小的最大整数
* MOD(x,y);//去模
* RAND();
* ROUND(x,y);
* TRUNCATE(x,y);//返回数字x截断为y位小数的结果

## 日期和时间函数

* CURDATE();//当前日期
* CURTIME();
* NOW();//当前时间和日期
* UNIX_TIMESTAMP(date);
* FROM_UNIXTIME(unixtime);
* WEEK(date);
* YEAR(date);
* HOUR(time);
* MINUTE(time);
* MONTHNAME(date);//返回date的月份名
* DATE_FROMAT(date,fmt);//格式化
* DATE_ADD(date,INTERVAL expr type);//时间计算
* DATEDIFF(expr,expr2);//时间天数

##流程函数

* IF(value,t,f);
* IFNULL(value1,value2);
* CASE WHEN[value1]THEN[result]....ELSE[default] END;
* CASE[expr] WHEN[vaule1]THEN[result1]...ELSE[default]END;
