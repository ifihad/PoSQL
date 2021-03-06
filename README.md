![](logo.png)

# 友情提醒

> 数据库操作有风险，请谨慎对待！一旦出现问题，阴阳亦爱莫能助。切记，勿忘。

# PyPI 库

**主页**

posql · PyPI	https://pypi.org/project/posql/

**安装**

`pip install posql`

# 操作示例

```python
import posql

myconn = posql.mysql(passwd='Ycode01')
myconn.select_table('default', 'test')

""" 增
myconn.sql(0).insert({'domain': 'www.baidu.com', 'position': 'start'})
"""

""" 删
myconn.sql(0).where('`id` > 7').delete()
"""

""" 改
myconn.sql(0).where('`id` = 7').update({'position': 'end'})
"""

""" 查
results = myconn.select()
print(results)
"""

"""
results = myconn.where('`id` = 1').sql(1).select()
print(results)
"""

"""
results = myconn.order(field='id').limit(5).select()
print(results)
"""
```

# 计划支持

* [x] MySQL
* [ ] MongoDB
* [ ] Redis
* [ ] SQLite
* [ ] PostgreSQL

