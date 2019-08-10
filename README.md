# news opinions

### 2019/08/04
1. 初始化工程

2. 项目模块化，不同领域模型放在不同包中
    
    * `conf` : 存放项目配置文件相关，现在只是通过`flask`加载了，具体还未设置
    * `app/db`:存放数据库相关操作，可能涉及`CRUD`的简单操作，也可能涉及查询结果集到`model`的绑定
    * `app/models`:存放实体，比如`User`、`News`、`Opinions`等
    * `app/services`:具体业务逻辑操作
    * `app/routes`:用户请求到`server`后，请求转发及结果返回，不涉及业务逻辑操作
    * `utils`:常用工具集，比如日期转换、异常捕捉等
    
3. 添加测试模块`test`，编写程序过程中涉及大量本地调试，如果用main()函数测试容易导致程序混乱，添加`unittest`辅助测试

4. 前端资源文件

    * static:前端静态资源文件
      * img:图片、ico等
      * css:页面样式
      * js:页面动作
    * templates
      * Error:统一存放错误展示页面

5. 项目缺少部分

    * DB为配置
    * 日志未配置
    * 前端考虑要不要用flask的模版语言来处理，似乎可以解释，Vue是否要引入？

    

### 计划

1. 任务安排分配
   * 用github的wiki，添加新功能和设计
   * 用github的issues，添加功能bug
2. 项目统一提交到develop分支，每个人在自己本地环境创建分支订阅develop，正式且无任何bug代码才合并到master分支