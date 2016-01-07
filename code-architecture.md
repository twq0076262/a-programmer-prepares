# 3. 代码架构

## 参考资料

- [软件设计杂谈](http://mp.weixin.qq.com/s?__biz=MzA3NDM0ODQwMw==&mid=207078329&idx=1&sn=14070c2bc5f24af58e951c8a926964e0#rd)

# 3.1 设计模式

设计模式。

## 参考资料

- [蔡学镛架构设计方法](http://vdisk.weibo.com/s/q8FZMJO4W2qq)

# 3.1.1 常用的 Javascript 设计模式

## 参考资料

- [常用的 Javascript 设计模式](http://web.jobbole.com/29454/)

# 3.2 面向对象程序设计

## 参考资料

- [S.O.L.I.D：面向对象设计的头 5 大原则](http://mp.weixin.qq.com/s?__biz=MjM5OTA1MDUyMA==&mid=206096090&idx=2&sn=2853d260242f7eaf5cf8fe9a0a8a9811#rd)

# 3.2.1 继承

继承从代码复用的角度来说，特别好用，也特别容易被滥用和被错用。不恰当地使用继承导致的最大的一个特征就是高耦合。 在这里我要补充一点，耦合是一个特征，虽然大部分情况是缺陷的特征，但是当耦合成为需求的时候，耦合就不是缺陷了。耦合成为需求的例子在后面会提到。

## 总结

可见，代码复用也是分类别的，如果当初只是出于代码复用的目的而不区分类别和场景，就采用继承是不恰当的。我们应当考虑以上3点要素看是否符合，才能决定是否使用继承。就目前大多数的开发任务来看，继承出现的场景不多，主要还是代码复用的场景比较多，然而通过组合去进行代码复用显得要比继承麻烦一些，因为组合要求你有更强的抽象能力，继承则比较符合直觉。然而从未来可能产生的需求变化和维护成本来看，使用组合其实是很值得的。另外，当你发现你的继承超过2层的时候，你就要好好考虑是否这个继承的方案了，第三层继承正是滥用的开端。确定有必要之后，再进行更多层次的继承。

## 参考资料

- [跳出面向对象思想(一) 继承](http://casatwy.com/tiao-chu-mian-xiang-dui-xiang-si-xiang-yi-ji-cheng.html)

# 3.2.2 多态

## 总结

多态在面向对象程序中的应用相当广泛，只要有继承的地方，或多或少都会用到多态。然而多态比起继承来，更容易被不明不白地使用，一切看起来都那么顺其自然。在客户程序员这边，一般是只要多态是可行方案的一种，到最后大部分都会采用多态的方案来解决问题。

然而多态正如它名字中所暗示的，它有非常大的潜在可能引入不属于对象初衷的逻辑，巨大的灵活性也导致客户程序员在面对问题的时候不太愿意采用其他相对更优的方案，比如 IOP。在决定是否采用多态时，我们要有一个清晰的角色概念，做好角色细分，不要角色混乱。该是拦截器的，就给他制定一个拦截器接口，由另一个对象（逻辑上的另一个对象，当然也可以是自己）去实现接口里的方法集。不要让一个对象在逻辑上既是拦截器又是业务模块。这样才方便未来的维护。另外也要注意被覆重方法的作用，如果只是单纯为了提供父类所需要的中间数据的，一律都用 IOP，这是比直接采用多态更优的方案。

IOP 能够带来的好处当然不止文中写到的这些，它在其他场合也有非常好的应用，它最主要的好处就在于分离了定义和实现，并且能够带来更高的灵活性，灵活到既可以对语言过高的自由度有一个限制，也可以灵活到允许同一接口的不同实现能够合理地组合。在架构设计方面是个非常重要的思想。

## 参考资料

- [跳出面向对象思想(二) 多态](http://casatwy.com/tiao-chu-mian-xiang-dui-xiang-si-xiang-er-duo-tai.html)

# 3.2.3 封装

# 3.3 面向接口编程

IOP。