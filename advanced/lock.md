# Lock

## Redis

* 核心函数
  * def set(self, name, value, ex=None, px=None, nx=False, xx=False):
  * def setex(self, name, time, value):

## RedisExtensions

* 相关函数
  * def acquire_lock(self, lockname, ex=None, acquire_timeout=10):
  * def release_lock(self, lockname, identifier):

* 示例
  ```python
  In [1]: import redis_extensions as redis

  In [2]: r = redis.StrictRedisExtensions(host='localhost', port=6379, db=0)

  In [3]: r.acquire_lock('redis_extensions')
  Out[3]: '026ad2a7-2b58-435f-8ba2-467458a687f1'

  In [4]: r.acquire_lock('redis_extensions')
  Out[4]: False

  In [5]: r.release_lock('redis_extensions', '026ad2a7-2b58-435f-8ba2-467458a687f1')
  Out[5]: True

  In [6]: r.acquire_lock('redis_extensions', ex=10)
  Out[6]: '84f6b991-7c30-4210-947a-deb56bbc769a'

  In [7]: r.exists('redis:extensions:lock:redis_extensions')
  Out[7]: True

  In [8]: # 10 Seconds Later

  In [9]: r.exists('redis:extensions:lock:redis_extensions')
  Out[9]: False
  ```
