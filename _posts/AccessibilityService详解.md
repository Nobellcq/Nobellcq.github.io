# 写在前头

这个对于理解View的分发，view的绘制什么的，有不错的帮助。



# Accessibility特点

## 生命周期由系统管理

可以在一个application里定义多个，如果你定义在lib里，那么这个AccessbilityService会提前初始化，定义在自己的application是无法提前初始化的。 这个特点可以用来做一些神奇的事情。 application里的只会在获得权限的时候 进行初始化 ， 这个就有意思了

## 其他特点

### toast无法正常运行，需要用appli上下文，且用Looper.prepare() 和 Looper.loop() 包围

# View特点

view会层叠，特别是Tab

# 疑惑

## 一个node是如何保存全部上下级关系的？

## node的时效性？ 可否缓存

## disconnected Node 又是什么呢

# API设计

## checkPageIsOk

当前页面是否加载完毕，用于卡得批爆的页面，加载过程中，node是不断增长的。但是怎么监测是个问题。node加载完毕，渲染也还需要一点时间

# 思想哲学

找 和 点 分开。

找里面再分过滤。

找和点完善后，再进行联系组合	

# 关于此类的App

google 的 TalkBack

https://github.com/penglu20/Bigbang  全能分词

全能取词 [BigBang](https://github.com/penglu20/Bigbang)， https://www.jianshu.com/p/60758b3f2c7c 比较好的一个点就是，通过反射获取当前点击view的viewId，从而变相的获取到当前点击的坐标，等等一系列信息，也是其原理。 附带提一个非本应用获取用户点击坐标的操作 https://blog.csdn.net/kunminxu/article/details/102758269



关于如何获得

# Idea 

可视化编程 结合blocky。或者更白痴的方法，点击一个点，自动解析该点，获取信息，后台智能生成。

