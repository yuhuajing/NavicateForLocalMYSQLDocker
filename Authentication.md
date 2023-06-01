# NavicateForLocalMYSQLDocker

question:
```javascript
2059 - Authentication plugin 'caching_sha2_password' cannot be loaded: dlopen(../Frameworks/caching_
```

we could solve the problem by doing this:
```golang
mysql -uroot -ppassword 
 
use mysql; 

# Attention, if remote call. replace 'localhost' with '%'
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '你的数据库密码';
 
FLUSH PRIVILEGES; 
```