## 本项目实现的最终作用是基于JSP民宿预订网站信息管理平台
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 会员管理
 - 新闻管理
 - 民宿信息管理
 - 用户管理
 - 留言管理
 - 管理员登录
### 第2个角色为用户角色，实现了如下功能：
 - 修改个人信息
 - 提交订单
 - 查看我的订单
 - 查看民宿信息
 - 查看留言板
 - 查看网站新闻
 - 用户登录与注册
## 数据库设计如下：
# 数据库设计文档

**数据库名：** msydxxpt

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [admin](#admin) | 管理员表 |
| [jiudian](#jiudian) |  |
| [kefang](#kefang) |  |
| [message](#message) | 留言信息表 |
| [news](#news) | 新闻资讯表 |
| [pingjia](#pingjia) |  |
| [userinfo](#userinfo) | 用户信息表 |
| [yuding](#yuding) |  |

**表名：** <a id="admin">admin</a>

**说明：** 管理员表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | userName |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  3   | userPw |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  4   | zhi |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  5   | tel |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  6   | age |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |

**表名：** <a id="jiudian">jiudian</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  3   | dizhi |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  4   | style |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | info |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  6   | pic |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  7   | tel |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |

**表名：** <a id="kefang">kefang</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | jid |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  4   | chuang |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | ren |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  6   | price |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 价格  |
|  7   | TYPE |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 类型  |
|  8   | state |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 状态  |

**表名：** <a id="message">message</a>

**说明：** 留言信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | msg |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  3   | appuser |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  4   | date |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  5   | reply |   text   | 65535 |   0    |    Y     |  N   |   NULL    | 回复  |

**表名：** <a id="news">news</a>

**说明：** 新闻资讯表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  3   | date |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  4   | info |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  5   | appuser |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  6   | pic |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |

**表名：** <a id="pingjia">pingjia</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | msg |   text   | 65535 |   0    |    Y     |  N   |   NULL    |   |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  4   | adddate |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 添加时间  |
|  5   | jid |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="userinfo">userinfo</a>

**说明：** 用户信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  3   | pwd |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  4   | sex |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  5   | age |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  6   | tel |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  7   | address |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  8   | email |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  9   | grade |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |

**表名：** <a id="yuding">yuding</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  3   | fang |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  4   | count |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  5   | bdate |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  6   | edate |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  7   | tel |   varchar   | 255 |   0    |    Y     |  N   |   ''    |   |
|  8   | fangkuan |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  9   | dingjin |   double   | 23 |   0    |    Y     |  N   |   NULL    |   |
|  10   | ism |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  11   | mtel |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**运行不出来可以微信 javape 我的公众号：源码码头**
