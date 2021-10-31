# zxl
本项目需要先创建Mysql数据库
下面是创建语句
create database mydb; #建立数据库
use mydb;             #进入到数据库

#课程表
CREATE TABLE `c` (
   `cno` int NOT NULL,                    #课程编号                         
   `cname` varchar(45) DEFAULT NULL,      #课程名
   `cx` varchar(45) DEFAULT NULL,         #课程性质
   `cs` double DEFAULT NULL,              #课程授课学时
   `ct` double DEFAULT NULL,              #课程学分
   `cnum` int DEFAULT NULL,               #课程已选人数
   `cl` int DEFAULT NULL,                 #课程人数上限
   PRIMARY KEY (`cno`)
 ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

#学生表
CREATE TABLE `s` (
   `sno` int NOT NULL AUTO_INCREMENT,     #学生学号
   `sname` varchar(45) DEFAULT NULL,      #学生姓名     
   PRIMARY KEY (`sno`)
 ) ENGINE=InnoDB AUTO_INCREMENT=1000 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

#选课表
CREATE TABLE `sc` (
   `sno` int NOT NULL,                    #学号
   `cno` varchar(45) NOT NULL,            #课程编号
   PRIMARY KEY (`sno`,`cno`)
 ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
 
 执行make前需要修改Main.c中连接数据库的参数
