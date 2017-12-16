# githunTest
大话设计模式的ts代码

## 01简单工厂
- 面相对象通过封装、继承、多态把程序的耦合度降低。
- 聚合表示一种弱的‘拥有’关系，体现的是A对象可以包含B对象，但B对象不是A对象的一部分。 雁群 - 大雁
- 合成（组合）是一种强‘拥有’关系，体现了严格的部分和整体的关系，部分和整体的生命周期是一样的。鸟 - 翅膀

## 02策略模式
- 面相对象编程不是类越多越好，类的划分是为了封装，分类的基础是抽象，具有相同属性和功能的对象的抽象集合是类。

- 策略模式是一种定义一系列算法的方法，这些算法从定义上看做相同的工作，但是实现不同。它可以用相同的方式调用所有算法，减少了各种算法类与使用算法类之间的耦合。
- 策略模式的Strategy类层次为Context定义类一系列的可供重用的算法或行为。继承有助于析取这些算法中的公共功能。
- 策略模式简化了单元测试，因为每个算法都有自己的类，可以通过自己的接口单独测试。
- 当不同的行为堆砌在一个类中时，就很难避险使用条件语句来选择合适的行为。将这些行为封装在一个个独立的Strategy类中，可以在使用这些行为的类中消除条件语句。
- 策略模式封装了变化---策略模式就是用来封装算法的，但在实践中，我们发现可以用它来封装几乎任何类型的规则，只要在分析过程中听到需要在不同时间应用不同的业务规则，就可以考虑使用策略模式来处理。
- 在基本的策略模式中，选择所用具体实现的职责由客户端对象承担，并转给策略模式的Context对象。
- 任何需求变更都是需要成本的。

## 03单一职责原则 --- SRP
- SRP：就一个类而言，应该仅有一个引起它变化的原因
- 软件设计真正要做的许多内容，就是发现职责并把那些职责相互分离。
- 如果一个类承担的职责过多，就等于把这些职责耦合在一起，一个职责变化可能会削弱或者抑制这个类完成其他职责的能力。这种耦合会导致脆弱的设计，当变化发生时，设计会遭受到意想不到的破坏。
- 如果你能够想到多于一个的动机去改变一个类，那么这个类就具有多于一个的职责。此时应考虑职责分离。

## 04开闭原则 --- OCP
- OCP：开放-封闭原则，是说软件实体（类，模块，函数等）应该可以被扩展，但是不可以被修改。即，对于扩展是开放的，对于修改是关闭的。
- 怎样的设计才能面对需求的改变却可以保持相对稳定，从而使得系统可以在第一个版本以后不断推出新的版本呢？
- 无论模块是多么的封闭，都会存在一些无法对之封闭的变化。既然不可能完全封闭，设计人员必须对于他设计的模块应该对哪种变化封闭作出选择，它必须先猜测出最有可能发生变化的种类，然后构造抽象来隔离那些变化。
- 等到变化发生时立刻采取行动。
- 在我们最初编写代码时，假设变化不发生。当变化发生时，我们就要创建抽象来隔离以后发生的同类变化。
- 面对需求，对程序的改动时通过增加新代码进行的，而不是更改现有的代码。
- 我们希望的是在开发工作展开不久就知道可能发生的变化，查明可能发生的变化所等待的时间越长，要创建正确的抽象就越困难。
- 开闭原则是oop设计的核心所在。遵循这个原则可以带来面相对象技术所声称的句法好处，也就是可维护，可扩展，可复用，灵活性好。开发人员应该仅对程序中呈现出频繁变化的那些部分抽象，然而，对于应用程序中的每个部分都刻意地进行抽象同样不是一个好主意。拒绝不成熟的抽象和抽象本身一样重要。