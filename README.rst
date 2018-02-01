gherkinDB
--------

gherkinDB is lightweight, fast, and simple database based `pickleDB <https://pythonhosted.org/pickleDB/>`_. 


```````````````

    >>> import gherkinDB

    >>> db = gherkinDB.load('test.db', False)

    >>> db.set('key', 'value')

    >>> db.get('key')
    'value'

    >>> db.dump()
    True
