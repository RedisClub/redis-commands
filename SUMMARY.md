# Redis 命令详解

## 脑图

* [Redis-commands@naotu.baidu](http://naotu.baidu.com/file/859b1bbb33f281328ad9687a6b73018c?token=372a0cf7a29907b1)

## 命令

* Cluster - 集群
* Connection - 连接
* [Geo - 地理位置](commands/Geo/README.md)
  * 增加
    * [GEOADD - 添加/修改地理位置坐标](commands/Geo/geoadd.md)
  * 删除
    * GEOREM(ZREM) - 删除地理位置坐标
  * 修改
    * [GEOADD - 添加/修改地理位置坐标](commands/Geo/geoadd.md)
  * 查询
    * GEOPOS - 获取地理位置坐标
    * GEOHASH - 获取地址位置HASH值
    * GEODIST - 获取两个地址位置距离
    * GEORADIUS - 获取指定范围元素(指定经纬度作为中间点)
    * GEORADIUSBYMEMBER - 获取指定范围元素(已存储地理位置作为中间点)
  * 其他
* Hashes - 哈希
* HyperLogLog - xx
* Keys - 键
* Lists - 列表
* Pub/Sub - 发布/订阅
* Scripting - 脚本
* Server - 服务器
* Sets - 集合
* Sorted Sets(ZSets) - 有序集合
  * 增加
    * ZADD - 添加/更新元素
  * 删除
    * ZREM - 删除指定元素
    * ZREMRANGEBYRANK - 按排名删除元素
    * ZREMRANGEBYSCORE - 按Score删除元素
    * ZREMRANGEBYLEX - 按字典序删除元素
  * 修改
  * 查询
  * 其他
* Strings - 字符串
* Transactions - 事务

## 进阶

* Lock - 锁
* Signin - 签到
* Verification Code - 验证码
* Graphic Verification Code - 图形验证码
* Active Users - 活跃用户

## 专题

* [Distlock - 分布式锁](topics/distlock.md)

## 命令文档监测服务

* 监测对象 - https://redis.io/commands
