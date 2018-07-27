# DesignPatterns
Design Patterns with various real life scenarios


## Decorator
* Category: Structural
* Intent:
  Inject additional responsibilities	to	an existing	object dynamically. Decorators	
  provide	a	flexible	alternative	to	subclassing.
	Decorator	has	both	an	is‐a	and	a	has‐a	relationship	to	
its	base	class.

![decoratorpattern](https://user-images.githubusercontent.com/6056609/43302516-ab9cc3ea-9188-11e8-82e5-cc85c8e594fc.png)

## Decorator Example : Momos Store

Decorator pattern usecase explained with one real life example as Momos store with different types of Momo Decorators.
For examples, abstract 'Momos' class used to create concreate Momos like Veg Momo and Non-Veg Momos.

Also abstract 'MomoDecorator' created by inheriting from 'Momo' interface, and different Decorator created like 'Fried Momo', 'Shezvan Momo', 'Chocolate Momo' etc.

