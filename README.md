> ### SQL文件: db/tables_ly_tomcat.sql
> ### 数据库配置：src/main/resources/application.yml
准备数据库表，
数据库:
表：
CREATE DATABASE IF NOT EXISTS `test`  DEFAULT CHARACTER SET utf8 ;
USE `test`;
CREATE TABLE `user` (
  `id` INT(11) NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(100) NOT NULL COMMENT '名字',
  `age` INT(3) NOT NULL COMMENT '年龄',
  `sex` CHAR(1) DEFAULT NULL COMMENT '性别',
  PRIMARY KEY (`id`)
) ENGINE=INNODB DEFAULT CHARSET=utf8;
COMMIT;

授权一个项目需要用的账户密码：
grant all on test.* to 'java'@'%' identified by 'java';
flush privileges;
