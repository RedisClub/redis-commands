# Active Users

## Redis

* 核心函数
  * def setbit(self, name, offset, value):
    ```python
    ResponseError: bit offset is not an integer or out of range
    ```
    * ``offset`` 必须为整型， 可以使用数据表中用户的唯一自增字段 ``id``。
  * def bitcount(self, key, start=None, end=None):

* 示例
  ```python
  In [1]: import redis

  In [2]: r = redis.StrictRedis(host='localhost', port=6379, db=0)

  In [3]: r.setbit('active:users', 100, 1)
  Out[3]: 0

  In [4]: r.setbit('active:users', 1000, 1)
  Out[4]: 0

  In [5]: r.bitcount('active:users')
  Out[5]: 2

  In [6]: r.setbit('active:users', 1000, 0)
  Out[6]: 1

  In [7]: r.setbit('active:users', 10000, 1)
  Out[7]: 0

  In [8]: r.bitcount('active:users')
  Out[8]: 2
  ```
