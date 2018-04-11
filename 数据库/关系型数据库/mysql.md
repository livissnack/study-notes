# mysql的学习心得

[![Travis branch](https://img.shields.io/travis/rust-lang/rust/master.svg)](https://github.com/livissnack)

#### start server
mysqld

#### start client
mysql -u root -p password -P 3306 -h localhost

#### show all databases
show databases;

#### change database
use ```da_name```;

#### see all tables
show tables;

#### see all columns info
show colimns from ```table_name```;

#### see table all column info
describe ```table_name```

#### create database
create database if not exists ```name```;

#### create table
create table if not exists ```table_name```(
  ```column_name``` ```column_type```,
  ...
);

#### column types
int
标准SQL中有*```INTEGER```*&*```SMALLINT```*，MYSQL中有:

| type        | bytes   |
| ------------|:-------:|
| TINYINT     | 1       |
| SMALLINT    | 2       |
| MEDIUMINT   | 3       |
| INT/INTEGET | 4       |
| BIGINT      | 8       |

显示长度
* 例如写```TINYINT(4)```表示显示4位，```TINYINT```有符号时最大为-128，且符号占1，长度为4

* 写上 ```INT(4)```, 插入一个长度为5的 11111, 依然可以正常显示出来