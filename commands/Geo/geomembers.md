# GEOMEMBERS

## ZRANGE

```shell
ZRANGE members 0 -1
```

## GEORADIUS

```shell
GEORADIUS members 0 0 +inf km
```

## 示例

```shell
$ redis-cli

# ZRANGE

127.0.0.1:6379> ZRANGE jscities 0 -1
1) "suzhou"
2) "wuxi"
3) "xuzhou"
4) "nanjing"

# GEORADIUS

127.0.0.1:6379> GEORADIUS jscities 0 0 +inf km
1) "suzhou"
2) "wuxi"
3) "xuzhou"
4) "nanjing"
```
