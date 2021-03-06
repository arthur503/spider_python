spider_python
=============

抓取北邮人论坛和水木社区校招信息的爬虫程序。

新增手机短信通知功能，需要在conf.py里配置139手机号，发件箱账号和密码。

爬取模块默认每1小时运行1次，同时抓取web_urls和current_message_urls。每爬取10次清空所有数据。

发短信模块默认每10分钟扫描一次current_message_urls，不为空才会发短信。发送成功后会把current_message_urls合并到outdated_message_urls中，并清空current_message_urls。


不支持Python3.

Unix/Windows下均需要先在本机安装[redis](http://redis.io)服务程序，然后在Unix下运行redis-server，在Windows下启动redis-server.exe。

安装示例：Mac OS X下安装redis

    brew install redis

此外，程序依赖以下Python第三方包：

* [APScheduler](http://pythonhosted.org/APScheduler)

* [BeautifulSoup 3.2.1](http://www.crummy.com/software/BeautifulSoup/bs3/documentation.zh.html)

* [redis-py](https://github.com/andymccurdy/redis-py)

* [requests](https://github.com/kennethreitz/requests)

安装示例：Mac OS X/Linux下安装Python第三方包
    
    pip install apscheduler
    pip install BeautifulSoup
    pip install redis
    pip install requests
    
然后直接运行main.py程序，访问<http://127.0.0.1:8888>
    
效果如下：

![1](https://lh4.googleusercontent.com/-DdobnB7RIf8/UhTs2OdrPNI/AAAAAAAAAM4/df2OmS0bhV0/w958-h599-no/%25E5%25B1%258F%25E5%25B9%2595%25E5%25BF%25AB%25E7%2585%25A7+2013-08-22+%25E4%25B8%258A%25E5%258D%258812.36.50.png)

Enjoy it。

