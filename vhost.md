虚拟主机的配置
------------------------------------
1.apache配置文件 的设置
    D:/wamp/bin/apache/apache2.4.18/conf/httpd.conf

    1).line 160 开启重写模块
    LoadModule rewrite_module modules/mod_rewrite.so

    2).line 250 访问权限 允许所有
    AllowOverride all
    Require all granted

    3).line 520 开启vhost配置文件
        Include conf/extra/httpd-vhosts.conf

2.httpd-vhost.conf 文件的设置
    D:\wamp\bin\apache\apache2.4.18\conf\extra
    
    <VirtualHost *:80>
        ServerName s52.com
        DocumentRoot d:/wamp/www/s51/web   #!(注意 文件路径为正斜线!!!)
    </VirtualHost>

3.系统的 host文件
    C:/Windows/System32/drivers/etc/hosts
    127.0.0.1 s52.com