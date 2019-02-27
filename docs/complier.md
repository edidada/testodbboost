# complier

```shell

odb -d mysql --profile boost --generate-schema --generate-query --generate-session employee.hxx
In file included from <odb-prologue-1>:1:0:
/usr/libexec/odb/x86_64-linux-gnu/include/odb/boost/date-time/mysql/gregorian-mapping.hxx:8:57: fatal error: boost/date_time/gregorian/gregorian_types.hpp: 没有那个文件或目录
 #include <boost/date_time/gregorian/gregorian_types.hpp>
                                                         ^
compilation terminated.

```

```shell

odb -d mysql --profile boost --generate-schema --generate-query --generate-session employee.hxx
odb -d mysql --profile boost --generate-schema --generate-query --generate-session employee.hxx
```

```shell

g++ -c person-odb.cxx
g++ -DDATABASE_MYSQL -c driver.cxx
g++ -o driver driver.o person-odb.o -lodb-mysql -lodb
```


```shell
scp person.sql root@60.205.225.118:~
scp employee.sql root@60.205.225.118:~
ssh root@60.205.225.118

mysql --user=root --password=5Edidada --database=odb_test < person.sql
mysql --user=root --password=5Edidada --database=odb_test < employee.sql

./driver --user root --password 5Edidada --database odb_test --host 60.205.225.118
```

执行结果

```shell

testodbcomposite --user root --password 5Edidada --database odb_test --host 60.205.225.118
Mr Joe Dirt <joe@example.com>
  nickname: Squeaky
  alias: Anthony Clean
  phone 1: 555 5555
  phone 2: 666 6666
Mr Joe Dirt

```
