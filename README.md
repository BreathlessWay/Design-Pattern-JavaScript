# Design-Pattern-JavaScript

## Javascript设计模式与开发实践的相关实例

### 基础概念
1. javascript为动态类型语言,在程序运行时才会确定变量类型
2. 多态: 同一操作作用于不同的对象上,可以产生不同的解释和不同地执行结果(javascript的变量类型在运行期间是可变的,所以javascript的多态性是与生俱来的)
3. javascript不存在类的概念,所以javascript中的对象都是从原型对象上克隆下来的,es5提供了克隆对象的api  `object.create()` 来实现原型继承
4. this: javascript中的this始终指向一个对象,基于函数的执行环境动态绑定的,箭头函数没有this,arguments,new.target的绑定
5. 构造函数中显示的返回一个对象的话,则new出来的实例为返回的对象而不是this
6. call,apply均可以改变this绑定,不同的是call第一个参数为this指向,后面可以有无限个参数,作为参数传入,apply第一个参数为this指向,第二个参数为一个数组,用来作为参数传递(类arguments),es5所提供的bind会产生一个新函数
7. 闭包: 函数返回一个函数,并且函数保持对上层作用域的引用
8. 节流:基于setTimeout
9. AOP:面向切面编程,将非业务代码抽离比如打点
10. new的过程: 创建一个新对象；->将构造函数的作用域赋给新对象（因此this就指向了这个新对象）；->执行构造函数中的代码（为这个新对象添加属性->返回新对象

### 设计模式
1. 单例模式: 保证一个类仅有一个实例,并提供一个访问它的全局访问点
2. 策略模式: 定义一系列的算法,把它们一个个的封装起来,并且使它们可以互相替换
3. 代理模式: javascript中常用的虚拟代理(将开销很大的对象延迟到需要的时候才创建),缓存代理(将执行结果缓存在闭包变量中)
4. 迭代器模式: 提供一种方法来顺序访问一个聚合对象中的各个元素
5. 发布-订阅模式: 又叫观察者模式,javascript中一般使用事件模型来驱动
6. 命令模式: 定义一系列的命令算法,将命令接收者和命令解偶,在javascript中命令模式是一种隐形模式
7. 组合模式: 将对象组合成树形结构,通过对象的多态性,使得用户对单个对象和组合对象的使用具有一致性
8. 模板方法模式: 包括两部分1⃣️抽象父类2⃣️具体的实现子类(java typescript中的 abstract 抽象类)
9. 享元模式: 用于性能优化,减少对象的创建,运用共享技术来有效支持大量细粒度的对象,划分内部状态和外部状态
10. 职责链模式: 一系列可能会处理请求的对象被连接成一条线,请求在对象之间传递,直到遇到可以处理请求的对象.请求发送中只需要知道链中的第一个节点
11. 中介者模式: 接触对象与对象之间的耦合,所有相关对象都通过中介者来通信,而不是互相引用
12. 装饰者模式: 给对象动态添加职责,将一个对象嵌入另一个对象中形成一条包装链,每层对象都处理请求

### 设计原则
1. 好莱坞原则: 允许底层组件将自己挂钩到高层组件中,二高层组件会决定何时以何种方式去使用这些底层组件,应用场景如发布订阅模式,回调函数,模版方法模式
