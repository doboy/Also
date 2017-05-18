from also import also, AlsoMetaClass

class Foo:
    __metaclass__ = AlsoMetaClass

    @also('getThing')
    @also('get_thing')
    def getthing(self):
        return 'go bears'

foo = Foo()
assert (foo.getthing() == foo.get_thing() == 
        foo.getThing() == 'go bears')

