#利用Travis CI 让你的github项目持续构建(Node.js为例)
    
   Travis CI 是目前新兴的开源持续集成构建项目，它与jenkins，GO的很明显的特别在于采用yaml格式，简洁清新独树一帜。目前大多数的github项目都已经移入到Travis CI的构建队列中，据说Travis CI每天运行超过4000次完整构建。对于做开源项目或者github的使用者，如果你的项目还没有加入Travis CI构建队列，那么我真的想对你说out了。

  搭建Travis CI build，需要你有个github账号和github项目：

1：用github账号登陆Travis CI.

2 :在右上角你的账户名点击进入 account，在Repositories tab页点击Sync now同步你的github项目，

3：选中项目将默认的off改变为on开启项目的持续集成。

4：在你项目的根目录建立一个.travis.yml文件，内容为：

language: node_js

node_js:  

     - 0.4  

     - 0.6

5: 在打开你的node.js的package.json文件，确保加入script/test节点：

"scripts": {
    "test": "XXXX"
  },

这里你可惜选择mak或者jasmine-node等node.js测试框架的测试命令。并且可以把依赖加入package的depends

6：在你项目中运行npm test，确保正常工作。

7： check in你的code到github，代开tracivs ci界面等待其同步并运行你的build构建。

 

  如果你需要将你的build构建状态放在一个显眼的位置或者项目readme，你可以在首页My Repositories中找到项目并设置中复制状态图片code，形如：

[![Build Status](https://travis-ci.org/greengerong/qing.png?branch=master)](https://travis-ci.org/greengerong/qing)

   Travs CI 支持多中语言如ruby，java的maven，gradle,Go等请参见文档[Travis Docs](http://about.travis-ci.org/docs/).

   在上面提到的travis.yml文件中我们还可以加入build前后执行脚本，形如：

before_script:  

     - before_command_1  

     - before_command_2

after_script:  

     - after_command_1 

     - after_command_2

 

   将你的开源项目加入Travis CI队列吧，很容易让你的项目加入持续集成，持续构建队列。