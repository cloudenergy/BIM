#BIM——Building Information Modeling（建筑信息模型）

##定义
BIM即建筑信息模型（Building Information Modeling）是以建筑工程项目的各项相关信息数据作为模型的基础，进行建筑模型的建立，通过数字信息仿真模拟建筑物所具有的真实信息。它具有可视化，协调性，模拟性，优化性和可出图性五大特点。

##意义

让建筑超越想像，全智能化可视，可管，可控。完成建筑生活更美好，能量消耗更绿色。

##实现

###[opensourcebim](http://bimserver.org/blog/)——In the heart of your BIM（BIM核心实现）
开源的BIM实现
  
![](http://7xiwlk.com1.z0.glb.clouddn.com/4880ac031018a5b425223b6946dd6edf.png)

图示各个工具介绍：[our tools are listed](https://github.com/opensourceBIM/AECHackathon/wiki)
主要工具包括

* [BIMserver](http://www.bimserver.org)
* [bimsurfer](http://bimsurfer.org)  
* [ bimvie.ws](http://opensourcebim.github.io/bimvie.ws-viewer)
* [BCF server](https://github.com/opensourceBIM/BCF-Forum/wiki/BCF-server)
* IFD server
* [ifcOPENShell](http://ifcopenshell.org)
* [bimQL](http://bimql.org)

###基于开源bimsurfer的bim浏览平台搭建
	1.详细需求：

        a)利用bimsurfer，bimserver搭建bim浏览平台。

        bimsurfer:http://bimsurfer.org/,https://github.com/opensourcebim/BIMsurfer

        bimserver:http://bimserver.org/

        要求：bimserver，bimsurfer尽量采用最新版本。如果确实有困难基于老版本也能接受。

        b)平台浏览效果要求：http://pan.baidu.com/s/14efts。https://github.com/halad/MOST_BIMsurfer 的效果视频

    2. 验收标准

        1.提供搭建好的平台及安装注意事项

        2.一周以内
        
###buildingSMART——standard interface for BIM in the cloud（BIM云端化接口）
BIM Service interface exchange （BIMSie）： [the standard API for BIM Web Services to get BIM in the cloud](https://buildingsmart.github.io/BIMSie/)

BIMSie：BIM web云端化接口  

BIM开始作为一个数据驱动的概念。文件与BIM数据交换和BIM数据的标准化是创新的一个重要组成部分。今天，BIM是越来越多的网络（“在云端”）。 BIM Web服务正在变得越来越受欢迎。大多数的这些在线BIM服务没有其他服务通知创建的，并且具有不同的，具体地为他们的任务而设计的技术接口（API）来进行通信。连接到这些应用程序有“手”来完成，并且是每个应用程序的不同。在线BIM服务（服务器/服务/等等）的API标准化创造了机会，以创新的行业BIM服务自动相互交融。
### [bimsync](https://bimsync.com/) —— your BIM in your browser（BIM云平台）
bimsync是一个类同化emoncms云平台化家庭能耗的云平台化BIM网站。包括[bimsync API](https://bimsync.com/developers/reference/api/1.0)，[bimsync web使用BIM](https://github.com/catenda)，[bimsync云计算中心](http://catenda.no/services)。

![](http://7xiwlk.com1.z0.glb.clouddn.com/1c76fe90430a1cc6deb9b16c998c61ad.png)      
![](http://7xiwlk.com1.z0.glb.clouddn.com/40f53d9f9f8fe1c86f5ee02822efa2cc.png)


###一些3D展示

* [基于webGL与threejs的openBIM的展现](https://github.com/opensourceBIM/WebGL-threeJS)
* [直接在BIM上读传感器数据](https://github.com/AaltoAsia/Otaniemi3D)，它竟然有六个分支。结合了google map。活跃度很高。
* [ 一个带假json数据纯前端演示demo](https://github.com/tariel-x/glbim)
* [博锐尚格的isagy BIM 展现](http://persagy.com/page/isagy.html)：博锐尚格iSagy-BIM能源管理平台由传感器网络、接入传输总线、能耗私有云计算平台、BIM、3D模型库、大数据智能挖掘系统、远程专家系统及节能决策中心共七部分组成。系统涵盖高精度测量与传感、现场总线及网络通信、云计算、人工智能、建筑节能、建筑信息模型等多个技术领域。系统包含5000余个能量计量装置及传感器设备，300余个数据采集与控制设备，高速通讯网络、服务器集群及图形工作站，节能管理中心内还安装了两个超大LED矩阵供管理人员实时观测与处理数据信息，其信息采集规模，数据处理能力，3D模型规模在国内外均首屈一指。

