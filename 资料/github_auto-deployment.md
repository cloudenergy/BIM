#github Auto-Deployment

最近在使用github组织私有库做团队协作工具，使用过后再加上仔细研究，发生真的挺屌的。

尤其github这个开放性，带来的持续集成能成，就有点像IFTTT，一切皆有可能。

这篇先讲github代码更新后，怎么自动在自己服务器上完成布暑

##github代码更新后自动署有两个办法

都是利用github的webhook功能。

* 一个是[利用webhook发一个post](http://www.tuicool.com/articles/2YR3IzN)到自己服务器上，自己写脚本来pull代码，完成布署。
* 一个是直接用户github提供的Add GitHub Auto-Deployment service功能。

### Git webhook agent for server auto-deployment 

利用webhooks有个好处，就是可以直接对组织或者针对某一个库做触。webhooks其实就是个触发机制，当你的组织或者你的库有任何风吹草动的时候，webhooks向你配置的指定URL发一个http POST请求。里面有详细描述告诉服务端github这边发生了什么，详细查看[webhooks文档](https://developer.github.com/webhooks/) 。文档里面清楚的讲明白[事件有哪些](https://developer.github.com/v3/activity/events/types/)，什么样的事件传给你什么样描述。[组织的webhooks](https://developer.github.com/v3/orgs/hooks/)又能干什么。

 那么就快乐的开始吧，先在github的组织或者库上，点setting，选中webhooks and service  
![](http://7xiwlk.com1.z0.glb.clouddn.com/8cd381518575a47295c60d4d7393e6d9.png)  

 接着在cloudenergy.me的服务上，写上一个auto-deployment的服务，样例可以参考[hookagent](https://github.com/mytharcher/hookagent)
 
 ![](http://7xiwlk.com1.z0.glb.clouddn.com/51cd87ad61410f4c911280d0b1eaf4e1.png)     
 
###Add GitHub Auto-Deployment service

不研究不知道，仔细一研究，发现github其实直接集成第三方的自动布署服务。这个Auto-Deployment service由[atmos](http://www.atmos.org)提供的[GitHub Auto-Deployment](http://www.atmos.org/github-services/auto-deployment/)。这个文档有讲atmos的workflow是怎么实现的。

这个更简单了，在库首页点setting，选中webhooks and service  （这个只支持库，不支持组织，因为是代码自动布署）  

![](http://7xiwlk.com1.z0.glb.clouddn.com/1dd3b3fd793aa5ec58e10fd7652233c4.png)   

然后把Deployment所需要的参数都一一填写好。在配置Add GitHub Auto-Deployment service时有完整的要求。