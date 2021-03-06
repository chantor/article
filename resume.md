# 个人信息

- 谭明/男/1994
- 本科/西南交通大学(211)/计算机系
- 工作年限: 3~4年
- 技术博客: [http://www.jianshu.com/u/5a327aab786a](http://www.jianshu.com/u/5a327aab786a)（粉丝434）
- Github: [https://github.com/hirudy](https://github.com/hirudy)
- 掘金分享社区: [https://gold.xitu.io/user/57a3f37d8ac247005f19929d](https://gold.xitu.io/user/57a3f37d8ac247005f19929d)（粉丝3800）
- 期望职位: 后端工程师
- 手机: 18583709203
- 邮箱: hirudy@qq.com
- QQ: 841927469

# 技能清单

- 基础：常用数据结构与算法、linux操作系统、数据库原理、tcp/udp/http、dfa、部分设计模式、协程
- 程序语言工具：擅长java/php，熟悉python、javascript/html/css，了解c、lua
- 开发框架：熟悉yii等mvc框架、thrift、dubbo等rpc框架、熟悉spring/mybatis常用框架、了解workman、swoole等异步网络通信框架。
- 数据库：熟悉mysql、redis、rocketmq/beanstalk消息队列， 了解memcache、zookeeper、mongodb/kafka
- web容器：熟悉nginx, 了解apache
- 操作系统：熟悉linux/unix，熟悉crontab、shell
- 工程相关：熟悉git/hg/svn等代码管理工具、maven/pecl等包依赖关系处理、tapd/jinkens/禅道/阿里rap等项目管理工具, 了解git/jumpserver

# 课外书单
- 基础: 《算法-第4版》、《TCP/IP详解 卷一》、《Head First 设计模式》、《HTTP权威指南》(部分)
- 程序语言工具: 《Java核心技术 卷1/2》、《深入理解Java虚拟机》、《Java NIO》、《Java程序员修炼之道》、《PHP 核心技术与最佳实践》、《高性能PHP应用开发》、《Python参考手册》
- 数据库: 《深入浅出mysql》、《REDIS入门指南》、《Redis设计与实现》
- web前端: 《CSS权威指南》、《Javascript高级程序设计》、《HTML5与CSS3权威指南》
- 其他:《Hadoop实战》(部分)、《Lua中文教程》(部分)、《memcached权威指南》(部分)

# 工作经历与项目经验

## 分期乐（乐信集团、2017.03-至今）
乐信集团为一家美股上市的消费金融公司。旗下产品有桔子理财、鼎盛资产、分期乐商城。注册用户3000-4000万。客单价较高。

两次绩效考核一直是A(优秀)

主要业绩为：

#### 1.Tab项目
项目周期:11.01-11.16。职责：技术负责人(SE)
+ 负责项目进度把控，协调涉及项目成员多达18人，开发人员多达9人项目开发。
+ 负责项目后台开发、对接其他部门资源。
+ 最终高质量高效率（总监肯定）完成部门重量级入口控制。

#### 2.部门运营体系搭建
系统周期：一直优化中。职责：运营组负责人
+ 入职后，一直负责部门运营体系搭建
+ 根据运营四要素，人群、门槛、形式、激励，利用**责任链、观察者**等模式，参考QQ运营体系，搭建了该体系。
+ 现已对接三个业务方（信用卡还款、二类账户、联名卡）。
+ 将活动开发从原有的**8天**左右缩减至**2天**左右。
+ 目前一年多，该系统接入活动**80**多个。

+ 同时设计过有较高并发的秒杀系统单机qps为**500/s**（压测数据）。一次秒杀活动实际观察数据3台机器总qps为**2000pqs**。
+ 通过前后分离、热点隔离、缓存等方式，达到高性能、通过分布式集群、多级缓存方式达到高可用、可伸缩性。通过多次拦截、令牌、限制ip/用户、奖励确认、监控告警等方式做到安全可靠。

#### 3.工作之外的组件化。
除了正常需求，还将已有功能抽离出来，已提供给中心使用（25人）。目前包括：配置系统（OA+db+redis）、白名单服务（**分库分表**）、用户标签服务、分布式锁（redis+db，事务+多段锁技术）、广告系统。


## 掌游宝(2015.06 - 2017.03)
成都我趣科技公司的掌游宝是一款移动端游戏社区综合平台。注册用户3000万，日活200万。员工大部分是腾讯出来。

#### 1. 爬虫服务

在该公司中，主要业绩为利用消息队列、缓存、布隆过滤器、python多线程等等技术，搭建了一套完整的分布式爬虫体系。
具体如下：

- lol战绩查询：lol战绩查询对于玩lol游戏的人来说是一项必备的功能，我们需要从tgp获取数据。tgp不会自己给我们数据，我和我leader设计了一套系统(magnet)来完成该数据的实时性获取，在客户端嵌入lua解析数据。作为具体是实施者，我完成了lua脚本的编写，lua脚本的维护升级，完成服务器端的具体实现。最后，我们使用2台服务器完成了支撑起我们lol战绩查询需求，接口调用量在`30万/小时`。至少还可以支持一倍的调用量。

- 视频解析：作为一个资讯平台，视频的观看是必不可少的。之前，我们视频观看时常有播放不了的情况，开始我们有一个简单视频解析服务。该服务完全不能提供所有服务，我做了如下几点优化：1.在该服务之前添加网关层，拦截掉所有相同的请求，同样的视频源地址在一段时间内只放出一个有效请求。该步达到拦截掉`60%`相同请求的效果。2.客户端嵌入lua解析，优先客户端解析，解析不了的在调用服务器解析。最终，支撑起我们所有平台的视频服务。接口调用量达`100万/小时`。

- 守望先锋战绩查询：守望先锋战绩查询对于玩守望先锋的人是一项必备的功能，在国服战绩可查的时候，为了完成比我们的竞争对手Max+更好更快的实现该功能。我设计实施了该服务
。在此之后，不断的与官网做矛与盾的较量。最后，完成圆满预定目标，获得当月公司`最高kpi考核-S`。

- 定时爬虫服务：对于某些统计数据，如英雄榜，玩家排行榜，这些公共数据不需要较为实时的获取。对于公司而言，我最终达到了数据提供的目的；对于个人而言，在完成各个任务的过程中，逐渐形成了自己的爬虫体系，并提取成一个框架叫TSpider，开源在github上我自己的仓库中。

- 离线爬虫系统：一个新的产品叫快上车，类似于内涵段子一样的，提供短文字、图片、视频，需要动态数据。我设计实现了一个离线爬虫系统，后台通过添加支持的三方服务。获取数据，完成对多个三方网站的爬取与维护。具体设计架构参见我的博客《2016年，我对爬虫的总结》。目前动态增长量为`5000/天`。

#### 2. 脏词过滤服务
作为一种平台，每天用户产生大量的ugc，脏词过滤就很有必要了。最初，我们的服务实现是
将一条ugc内容通过所有脏词for循环遍历替换。效率低下，我主要干的事情是使用DFA脏词过滤算法（核心是创建TrieTree）来重构脏词查找。达到的目的：脏词过滤的时间复杂度不会随着脏词库数量的增加而增大。

#### 3. 其他

dnf时装模拟数据、lol web页面改造、腾讯IM即时通讯接入、优酷视频上传、内容运营数据统计、chaoorder日志统计服务、lol游戏新老架构迁移、捕鱼支付系统、文字直播/赛事弹幕服务（IM服务）、用户中心/充值支付服务、广告系统

## 实习僧(2014.05 - 2015.03)
个人创业项目，该项目开始于2013年，目前已拿到天使投资500万，百度搜索“实习生”词条第一行。

搭建其原始版本的web服务。一个典型的lamp + memcached。我是两个主程之一。我参与后端开发，负责前端开发。

# 最后

感谢您们在百忙之中阅读这份履历，诚挚的期望能得到面试的机会。手捧菲薄求职之书，心怀自信诚挚之念，我期待着能成为贵公司的一员！
