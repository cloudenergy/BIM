#Github Automated testing

前一篇文章我讲了下[Github Auto-Deployment](file://./Github Auto-Deployment.md).这一篇，我们来讲讲更为复杂的Github Automated testing。程序员们说我步子迈的太大了，自动布署，自动测试一块整，并且说自动测试是不可能的任务。

我当然知道完全靠自动测试找出所有的bug，当然是不可能的任务。但程序员们在自动化测试上酒鲜血，抛头颅，不可能没有卵用的。我决定研究研究。

先研究Github Automated testing，先得搞清楚有哪些代码自动测试工具。比如[Travis CI](http://docs.travis-ci.com)

##自动测试工具

###静态js代码测试工具

* [HTML validation](http://validator.w3.org/source/)   
* [JSHint](http://jshint.com/about/)  
* [Cppcheck](http://cppcheck.sourceforge.net)  

###单元测试用例
自己写test单元测试用例

###自动化测试工具

* [Travis CI](http://docs.travis-ci.com/)
* [Jenkins CI](http://jenkins-ci.org/)
* [Web-CAT](http://web-cat.org/)
*[ CodeClimate](https://codeclimate.com/)
* [Coveralls](https://coveralls.io/)

##Github集成自动化测试

###CI([持续集成](http://blog.csdn.net/leijiantian/article/details/7916483))
利用库的services的Add Travis CI，集成Travis CI，[提交代码时对代码做自动化测试](http://www.liaoqiqi.com/post/173)  
![](http://7xiwlk.com1.z0.glb.clouddn.com/b33e53e33c01a54c2a793bbb4a4bbe88.png)   

一个是在 CI 中，当开发人员 push 代码到指定的 repo 中，github（或 gitlab）就会通知 Jenkins 把代码 pull 下来，然后 build， test等等。这一自动化靠的就是 Webhooks。具体而言，我们在 repo 的设置中给出了一个与 Jenkins 对应项目相关的 URL，当 github 检测到这个 repo 有 push 事件发生，就会发送一个 HTTP 请求到刚才指定的 URL；Jenkins 监听到请求后就执行某些操作，具体就是根据该项目配置的 github 地址，执行 git pull 或 git clone 等等。

###测试覆盖率
利用库的services的Cobertura。
###代码质量(code smell)
利用库的services的Add CodeClimate，完成代码质量测试，[通过github提升自己](http://www.ituring.com.cn/article/179424)  
![](http://7xiwlk.com1.z0.glb.clouddn.com/74fe037b1be15bfc26039d0e1facb8d7.png) 