# Redis 命令详解

## 脑图

* [Redis-commands@naotu.baidu](http://naotu.baidu.com/file/859b1bbb33f281328ad9687a6b73018c?token=372a0cf7a29907b1)

## 命令

* Cluster - 集群
* Connection - 连接
* GEO - 地理位置
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
    * ZADD - 添加元素
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
