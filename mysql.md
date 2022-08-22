安装mysql服务:
mysqld --install

初始化mysql
mysql --initialize --console

初始化密码：rMmLbE1o&Cw
,FFrwl(L!759

启动mysql:
net start mysql
关闭:
net net stop mysql

登录mysql:
mysql -u root -p
密码:

创建新用户：
INSERT INTO user 
          (host, user, password, 
           select_priv, insert_priv, update_priv) 
           VALUES ('localhost', 'guest', 
           PASSWORD('guest123'), 'Y', 'Y', 'Y');
查看数据库
SHOW SCHEMAS;
show databases;

查看数据库中的表
show tables;
