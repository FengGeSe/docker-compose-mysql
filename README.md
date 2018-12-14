# 文件目录
* README.md 
* docker-compose.yaml   // 定义了mysql容器启动参数
* mysql
    * conf.d   // 挂载到容器中 /etc/mysql/conf.d
        * disable_strict_mode.cnf   // 关掉sql语法strict模式
        * docker.cnf
        * mysql.cnf
        * utf8mb4.cnf     // utf8mb4开启
    * data    // 挂载到容器中  /var/lib/mysql
        * log     // 挂载到容器中  /var/log/mysql
            * error.log      // 文件权限 -rwxr-xr-x  否则写如不了日志
            * mysql.log      // 文件权限 -rwxr-xr-x  否则写如不了日志
    * mysql.conf.d    // 挂载到容器中  /etc/mysql/mysql.conf.d
            * mysqld.cnf
