# gherkinDB

gherkinDB is lightweight, fast, and simple database based `pickleDB <https://pythonhosted.org/pickleDB/>`_. 

While pickleDB went the way of using simplejson for speed, and is an awesome baby database for storing 
data, it lacked the ability to store complex data. Thus, gherkinDB was born. Similar to pickleDB, but closer
to its original roots; gherkinDB uses the dill package to load and save data to file, and a serializer was 
added into the base functionality. 


```python

import gherkindb

db = gherkindb.load('test1.db', True)

db.set('key', 'value')

# Outputs: value
print(db.get('key'))

# Added serialization functionality
def my_func():
    print("Much better!")

db.sset('func', my_func)

# Outputs: Much better!
db.sget('func')()

# Also :

# Outputs: Much better!
reborn = db.sget('func')

reborn()

```
