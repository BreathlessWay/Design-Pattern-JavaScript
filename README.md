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

### 设计模式
1. 单例模式: 保证一个类仅有一个实例,并提供一个访问它的全局访问点
2. 策略模式: 定义一系列的算法,把它们一个个的封装起来,并且使它们可以互相替换
3. 代理模式: javascript中常用的虚拟代理(将开销很大的对象延迟到需要的时候才创建),缓存代理(将执行结果缓存在闭包变量中)
4. 迭代器模式: 提供一种方法来顺序访问一个聚合对象中的各个元素
5. 发布-订阅模式: 又叫观察者模式,javascript中一般使用事件模型来驱动
