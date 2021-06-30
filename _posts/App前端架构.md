# 核心部分
Accore的设计部分，不可以将 service的配置文件xml放在lib里，这样是出现不了配置文件的


# App mobile端部分
js创建桌面快捷图标 android 



## dex加载技术 

不落地加载，直接从网络加载，最重要的是被从内存中dump出来

同时考虑两种android jvm 运行时，dalvk和art

https://github.com/yangkun19921001/DexEncryptionDecryption

我使用的dex加密算法 https://my.oschina.net/u/4374580/blog/4482028



### 进阶版升级到 shadow

这个作为多功能性应用应该是一个不错的选择

js作为前端，或者其他快速开发的，类似于小程序的

rhino是否需要接入，这样的话很多语言都能接入呀



# 悬浮窗

悬浮窗  贴边，单点启动，长按就那个

单是原地单点和拖动不可以重合

点击和拖动并存的问题 

事件不被group消费 https://segmentfault.com/a/1190000039196832

https://www.pianshen.com/article/8719548396/

重点就是这个dispatchTouchEvent

https://blog.csdn.net/bboyfeiyu/article/details/39719543









# 安全部分

## http 或者 https ，

## ws加密 ， 

## ws在线反钓鱼 实时验证 暗桩 验证一些只有服务度可以验证的

## dex加密：

后端自动加密，或者本地直接加密，客户端解密。加密的方法要写到底层 

加密方法：对文件byte数组进行AES加密

对于性能影响不大

考虑一个不落地加载 https://paper.seebug.org/59/  

加解密库 https://github.com/Forevery1/EncryptUtils

https://github.com/search?l=Java&q=byte%E5%8A%A0%E8%A7%A3%E5%AF%86&type=Repositories

## app混淆、缩小

## app加固

企业级加固尽量





# 性能部分，智能算法部分

如何获取当前的ANR程度，可以做一个适配，没啥意义，这是一个智能算法的部分。

智能停止部分

如果不用的时候，暂停掉，屏蔽接收对手机流畅度会好一点吗？ 还是系统有自带这样的服务，disableSelf,但是这样会不会导致服务权限失去



# 推荐模块

首页进行推荐，获取当前手机列表的信息，横向滑动进行推荐



