# GEO

## 实现方案

* 使用 GeoHash 进行地理位置坐标转换；
* 使用有序集合（Sorted Sets）存储转换后的 GeoHash。

## 经纬度

* longitude - 经度
* latitude - 纬度

## GeoHash
* [Ardb: A High Performance Persistent NoSql, Full Redis-Protocol Compatibility](https://github.com/yinqiwen/ardb)

## 精度问题

由于精度问题， 经纬度返回值可能与添加的值略有差异。

```
$ redis-cli
127.0.0.1:6379> GEOADD jscities 118.7964667635 32.0583898428 nanjing
(integer) 1
127.0.0.1:6379> GEORADIUS jscities 0 0 +inf km WITHDIST WITHCOORD WITHHASH
1) 1) "nanjing"
   2) "12690.3180"
   3) (integer) 4066006847826700
   4) 1) "118.7964668869972229"
      2) "32.05838900488951282"
```

添加的经纬度为 (``118.7964667635``, ``32.0583898428``)， 而返回的经纬度为 (``118.7964668869972229``, ``32.05838900488951282``)。

## 经纬度数据来源
* http://www.gpsspg.com/maps.htm
