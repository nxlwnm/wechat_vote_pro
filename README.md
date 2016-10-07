# wechat_vote_pro
去年写的vote的升级版，改用django编写

详细的使用说明和配置步骤要等逻辑能跑起来后再写了，目前已经完成的部分能跑通

对比以前的改进：
1，大幅增强自动化程度，以前配置环境时要改的地方很多，敲的命令也多，现在的设计都在尽量向着精简配置难度的方向进行
2，把一些配置时需要修改的函数独立出来，方便适应不同的选举环境。原有的设计只能进行x选x，碰到一些学院要求一些复杂的规则时基本抓瞎，代码都没法改
3，通过修改配置，能快速进行多轮投票，不像以前最多只能进行2轮，现在只需简单修改配置就可以快速适应

沿袭的地方：
1，流程控制有所修改，但是大体思想不变
2，数据库设计思想没变

目前已完成：
1，django框架的配置
2，数据库的设计和迁移，简化数据库，导入数据库的自动化，目前只需要django自带命令2个(搭建数据库框架，这个没法少)，python命令1个(导入投票人和被投票人，一键，不过生成验证码还是得用以前的)
3，自己写了个简单的微信公众平台SDK，不过功能还很简单，只是写了要用到的平台对接和文字消息的处理，以后如果有兴趣的话可以自己实现一个python版的SDK(目前只发现了PHP有SDK，这点太蛋疼了)
4，主体逻辑框架已完成，已实现未注册用户的处理

未完成：
1，投票人和管理员的流程控制
2，前端，不过按目前的估计，要改的地方不多，基本可以沿用
3，流程控制还有一些地方不太明确，需要点时间设计一下