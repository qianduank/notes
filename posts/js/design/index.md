# 前端设计模式

## 设计模式六大原则

- 开闭原则（Open Close Principle）

理解开闭原则，就要了解开和闭。这里的开是指对扩展开放，闭是说对修改关闭。想想我们有一套实现、提供一个服务，这样的程序需要能够随时进行扩展、随时支持第三方的自定义配置，但是不能去修改已用的实现代码。

比如我们做了一个 UI 组件轮子，业务方在使用时显然不能够修改我们的代码，但是仍然可以进行扩展。再比如著名的 Draft.js 库，在实现一个编辑器时，提供了灵活的插件机制，实现了热插拔效果，使得整个程序的扩展性好，易于维护和升级。甚至 Redux 库、Koa 库等基本所有库都有开闭原则的体现。

对于面向对象类型的语言来说，想要严格遵守开闭原则，往往需要使用接口和抽象类，这个我们会在具体设计中再次提到。

- 里氏替换原则（Liskov Substitution Principle）

里氏代换原则就稍微有些抽象，但它是面向对象设计的基本原则之一。

> 里氏代换原则要求，任何基类可以发挥作用的地方，子类一定可以发挥作用。

这句话怎么理解呢？想想我们的继承实现，里氏替换原则就是继承复用的基础。只有当派生类可以随时替换掉其基类，同时功能不被破坏，基类的方法仍然能被使用，这才是真正的继承，继承才能真正地实现复用，当然，派生类也需要随时能够在基类的基础上增加新的行为。

事实上，里氏代换原则是对开闭原则的补充。

- 依赖反转原则（Dependence Inversion Principle）

该原则要求针对接口编程，依赖于抽象。

- 接口隔离原则（Interface Segregation Principle）

接口隔离的意思或者目的是减少耦合的出现。在大型软件架构中，使用多个相互隔离的接口，一定比使用单个大而全的接口要好。

- 最少知道原则，又称迪米特法则（Demeter Principle）

最少知道顾名思义，是指：一个系统的功能模块应该最大限度地不知晓其他模块的出现，减少感知，模块应相对独立。

- 合成复用原则（Composite Reuse Principle）

合成复用原则是指：尽量使用合成 / 聚合的方式，而不是使用继承。这是很有意思的一点，我们在之前的课程中提到过：基于原型的继承在很多程度上「优于」基于类的继承，原因就在于基于原型的继承模式体现了可组合性，能够规避「大猩猩和香蕉」等问题的出现。组合是非常优秀的编程思想，这一点在函数式编程范畴中得到了最大程度的印证。

## 设计模式的三大类型和二十三种套路

设计模式并没有什么困难的，大体上所有的设计模式可以归结为三大类：

### 创建型

- 简单工厂模式

- 工厂方法模式

- 抽象工厂模式

- 建造者模式

- 单例模式

创建型的五种设计模式提供了更加灵活的对象创建方式，同时可以隐藏创建的具体逻辑。与直接使用 new 运算符实例化对象相比，这些模式具有更强的灵活性以及可定制性。

### 结构型

- 适配器模式

- 桥模式

- 组合模式

- 装饰器模式

- 外观模式

- 享元模式

- 代理模式

结构型的七种设计模式关注类和对象的组合，结合继承的概念，这些设计模式能使得对象具有更加灵活的功能设定。

### 行为型

- 职责链模式

- 命令模式

- 迭代器模式

- 中介者模式

- 备忘录模式

- 观察者模式

- 访问者模式

- 策略模式

- 状态模式

- 模板方法模式

- 解释器模式

行为型的十一种设计模式聚焦于对象和类之间的通信，这是构建大型程序架构必不可少的环节。

## 关于设计模式的学习

[Learning JavaScript Design Patterns](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)：addyosmani 大神的书 pdf

[JsPattern-ES6](https://github.com/DavidCai1993/JsPatterns-ES6): 使用 ES6 重写了《JavaScript 模式》一书中的样例

[es6-design-patterns](http://loredanacirstea.github.io/es6-design-patterns/#composite): 神器，这个网站通过 UML 图解释设计模式，同时配以可以运行的代码示例，非常方便对每一种设计模式进行学习。