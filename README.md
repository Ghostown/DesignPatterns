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

![decoratorpattern - copy](https://user-images.githubusercontent.com/6056609/43304294-2b0a2f48-9191-11e8-90dc-e00371a7578a.png)

* The Decorator pattern is implemented with C++11 code. This code explains how the Momo objects are decorated at runtime without changing there behaviour? Following screenshot shows Veg Momo object decorated with FriedMomo Decorator and ChocolateMomo Decorator.

* Driver code for Momo Store
```C
 MomoStore store;

    //Veg momo -> Decorated with Shalow Fry
    std::shared_ptr<VegMomo> vegmomo = std::make_shared<VegMomo>("Green vegitables");
    std::shared_ptr<FriedMomo> friedmomo = std::make_shared<FriedMomo>(vegmomo.get());
    store.addOrder(friedmomo.get());

    //NonVeg momo -> Decorated with Shezvan sauce
    std::shared_ptr<NonVegMomo> nonVegMomo = std::make_shared<NonVegMomo>("Chicken");
    std::shared_ptr<ShezvanMomo> szmomo = std::make_shared<ShezvanMomo>(nonVegMomo.get());
    store.addOrder(szmomo.get());

    //Veg momo -> Decorate with Fry -> Decorated with chocolate
    std::shared_ptr<VegMomo> vegmomo1 = std::make_shared<VegMomo>("Cryspy items");
    std::shared_ptr<FriedMomo> friedmomo1 = std::make_shared<FriedMomo>(vegmomo1.get());
    std::shared_ptr<ChocolateMomo> chocomomo = std::make_shared<ChocolateMomo>(friedmomo1.get());
    store.addOrder(chocomomo.get());

    store.executeOrders();
```

![objects](https://user-images.githubusercontent.com/6056609/43304796-131678c2-9193-11e8-9546-22b2d7fb26c5.png)
