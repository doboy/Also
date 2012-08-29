Also
====

Ever had a lot methods do the same thing? Guess not.. but for those rare occasions..

###### Trivial Example
```python
from also import also, AlsoMetaClass

class Foo:
    __metaclass__ = AlsoMetaClass

    @also('createFoo')
    def __init__(self, thing):
        self._thing = thing

    @also('getThing')
    @also('get_thing')
    def getthing(self):
        return self._thing

foo = Foo.createFoo('go bear')
assert (foo.getthing() == foo.get_thing() == 
        foo.getThing() == 'go bears')
```
