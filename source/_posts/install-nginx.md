title: 安装nginx记录
date: 2014-02-27 14:32:53
tags: [linux,nginx,记录]
---

安装步骤
---
{% codeblock lang:shell%}

	yum -y install pcre-devel openssl openssl-devel
	cd /usr/local/src
	wget http://nginx.org/download/nginx-0.7.68.tar.gz
	tar -zxvf nginx-0.7.68.tar.gz
	cd nginx-0.7.68
	./configure --with-http_stub_status_module
	make
	make install
	
{% endcodeblock %}
nginx_http_stub_status_module插件
---
这个模块能够获取Nginx自上次启动以来的工作状态。 此模块非核心模块，需要在编译的时候手动添加编译参数 `--with-http_stub_status_module`， 安装完成后需配置`/usr/local/nginx/conf/nginx.conf`使插件生效	


