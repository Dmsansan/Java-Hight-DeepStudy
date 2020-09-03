## Java并发编程案例

------------
author 司三三
date 2019-07-09
------------
    本次提交关于Java编程里面一个非常重要的一部分，就是Java的并发编程。使用Java并发编程的主要母的
    是提高代码的执行效率，以及并发服务产生时的可用性。当然，关于并发思想的一些概念性的东西就不做过
    多的介绍了。像什么并发编程的三要素、thread执行是的各种状态。这些需要自己网上找点资料看一下，本
    人推荐最好用书来学习，毕竟书是人类进步的阶梯！！！
    

找了一部分东西，一起研究一下，并发编程的实现业务特点以及实现方式。

本次代码实现的内容：
生产者  中间件  消费者

这三方有很多可以扩展的东西，以及用到的各部分组件就不介绍了。有一点编程经验的应该都清楚。
下面介绍一下这段代码实验的业务需求：
       
       生产者提供耶夫数据服务给中间件，消费者通过中间件消费资源。毕竟中间间的存储空间是有限的，当生产者提过的
       数据服务太大，或者消费者消耗过快就会导致一系列问题，我们需要用到并发编程思想来解决这些问题，比如控制生产者
       产生的数据服务，当中间件有存储空间的时候在提醒生产者提供消息数据服务，当中间件没有数据资源
       提醒消费者不进行消费，并且提醒生产者生产服务数据。 