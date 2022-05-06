# 1. 前言
拟定在这个项目中爬取[小说精品屋](http://47.106.243.172:8888/book/bookclass.html)的小说数据。为接下来的小说`App`提供后台数据内容。当然无论是爬虫项目、后台项目或者是小说`App`项目，仅用于学习目的。

# 2. 说明
爬虫部分使用`python`来编写，后台部分使用`kotlin`+`SpringBoot`来编写，`App`部分使用`Jetpack`来编写。虽然使用`kotlin`来编写爬虫，更有利于爬虫和后台的整合，可以设置一个定时任务来定时爬取数据。但是`python`写爬虫更加简单且之前也写过微博的爬虫自己也更加熟悉，所以还是采用`python`来编写爬虫。对于`App`部分，因为最近在学习`Jetpack`，可以说是为了练手。

* 爬虫项目：https://github.com/baiyazi/NovelApp/tree/main/xiaoshuoSpider
* 后台服务程序：https://github.com/baiyazi/NovelApp/tree/main/AppBackUp

# 3. 后记

记录一下开发日程：
* `2022`年`5`月`4`日：决定要做这个东西，以及部分爬虫程序编码；
* `2022`年`5`月`5`日：完成爬虫程序编码【简略版】，但感觉数据基本够用了，所以决定就不再考虑模拟分页来获取小说数据了。另：小说封面图片没有下载，需要后续完善。完成部分`SpringBoot`+`Mybatis`的整合，以及`Mybatis generator`插件的配置工作。
* `2022`年`5`月`6`日：完成`SpringBoot`后台数据接口的查询功能，添加对应的图片下载到本地服务器的`Controller`，规则为根据数据库中的`picURL`来生成一个唯一的`md5`值，然后将对应的这个图片使用`HttpURLConnection`来进行下载到本地磁盘。同时，将本地磁盘的这个目录配置为`SpringBoot`的静态资源访问路径，故而可以直接访问。
* `2022`年`5`月`6`日：准备着手开始写基于`Jetpack`的`App`项目。

