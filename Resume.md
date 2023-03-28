 <center>
     <h1>faaccy</h1>
     <div>
         <span>
             <img src="assets/envelope-solid.svg" width="18px">
             anyway2019@163.com
         </span>
         ·
         <span>
             <img src="assets/github-brands.svg" width="18px">
             <a href="https://github.com/faaccy">faaccy</a>
         </span>
     </div>
 </center>

 ## <img src="assets/info-circle-solid.svg" width="30px"> 个人信息 

- 生  日：1995.07.10
- 住  址：江苏省南京市
- 电 话：15261826280
- 邮 箱：anyway2019@163.com

## <img src="assets/graduation-cap-solid.svg" width="30px"> 教育经历
- 学  历：南京工业大学
- 专  业：信息与计算科学(一本)
- 其  他：CET6

## <img src="assets/briefcase-solid.svg" width="30px"> 工作经历


- #### **鼎捷软件** 2017.04-2019.06                	                    
  
  独立负责部门ERP产品与PMS、WMS等系统集成，涉及到跨部门协同工作，与超过200人包(含业务、客服、客户、基础架构组)沟通，期间通过多次主动整理并复用现有或者相似集成方案，以很小的时间成本部署方案，极大提高了整个部门的产出。最终复用被纳入部门标准工作流程。

  负责大型ERP产品需求分析，整理成标准文档，并使用自研框架(客户端winform）（后端WCF)撰写日常的定制化需求。负责新人业务与技术培训并参与验收。
 
- #### **巨泽科技** 2019.06-至今                	     

  现在主导PowerFun系列产品研发（室内骑行、划船机App）。参与过事务所(高新技术企业申报项目管理类的)项目的自动化申报,国外电商类产品的前端App(react-native)与后端业务的支持。

## <img src="assets/project-diagram-solid.svg" width="30px"> 项目经历

- **PowerFun**

  PowerFun Rider是一款室内骑行App（PC端/移动端），用户需要拥有一台室内骑行台或者功率计连接App可以在世界地图上选择一条感兴趣的线路，在室内体验真实线路的骑行.主要功能有：单人骑行，多人赛事，影子骑行。同时集成了心率计，踏频等硬件设备（硬件协议ANT+&le）并向strava等社交平台的分享骑行数据以及相关活动页面(**vue**)

  我在PowerFun Rider项目中承担了项目技术预演的责任，并推动了项目的快速迭代。该项目实现了室内骑行的App，细分功能包括单人骑行、多人赛事、影子骑行等。项目主要使用了PC端和移动端的技术，并需要用户拥有室内骑行台或功率计连接App，以在世界地图上选择感兴趣的线路，实现室内体验真实线路的骑行。

  整个项目主要经历了三个里程碑，每个里程碑都有着相应的技术难点和解决方案。在第一个里程碑中，我采用LayoutAnimation调用native端的动画处理，解决了动画卡顿的问题，并使用 native 的线程完成计时器的逻辑，提高了骑行成绩的准确性。为了节省客户端流量和电量消耗，我还优化了蓝牙连接部分，采用gzip算法压缩udp包大小，减少了客户端请求体大小。

  在第二个里程碑中，我遇到了chart点数过多、3d地图中线路点数过多等问题，导致渲染层卡顿或mesh过多问题，我通过改成可视区域内的线路显示，将性能得到了极大的提升。同时，我还将耗时的计算放到native端的线程中处理，实现了更好的性能表现。另外，我还优化了蓝牙连接部分，解决了设备连不上设备、扫描不到设备等问题。

  第三个里程碑是实现视频骑行或AR骑行的技术可行性验证，初步解析视频中摄像机运行轨迹并将其与unity结合，完成了国内第一个室内AR骑行的Beta版本。相应的技术难点包括学习camera solver相关技术，通过逆向工程快速完成多人骑行避让等交互效果，采用循环列表完成列表卡顿的问题和活动页面的按需加载。整个项目的三个里程碑都是承担了项目技术预演的责任，并通过技术解决方案推动项目的快速迭代和发展。

  用requetanimation 结合perfmance。Now构建前端高精度定时器用来渲染人物头像的移动
  利用原生线程完成逻定时器作为后端定时器完成逻辑层的数据采集，既保证了数据的准确性也保证了前端动画的流畅度（  解决了因为定时器不准导致的人物移动动画的抖动问题）

  untiy中我们遇到了有些线路过长导致绘制的LineRender占用了大量的内存和渲染压力，实现了可视区域内的动态绘制先炉，对于部分超过100km的线路卡顿问题。内存占用从原来的1g以上优化到 450MB左右。同时 从数据层面做了稀释减少了大量距离较近的gps的坐标。减少了mesh的胡绘制，

  坡度一场的问题，因为部分线路的来源数据并不包含海拔数据，使用google api获取的海拔数据存在误差就较大导致的坡度过高的问题,采用了滤波算法减少了异常坡度的问题，优化了用户骑行体验。

  对于线路相关数据采用本地缓存同时通过etag来确保本地数据的实时性，减少了用户每次骑行都要网络请求。

  对于运动相关的数据比较耗费cpu的数据转移到客户端减少了服务器cpu会100%的问题，导致服务器卡顿的问题。

  修改mapbox的native端源码的优化图片质量的优化已经相关手势功能完成业务需要。

  与设计师以及团队沟通，实现了Powerfun独有的风格的Button等独有空间，并且使用栈结构实现了简单的主要页面的路由功能，已经相关的goback 状态栏的风格变化等Route之类的，使得后续加入的同事能够在UI层的使用完成度达成一致的。

  划船机App chart图标的优化，由于业务需要折线图需要根据运动数据实时刷新，优化了chart每次绘制都要clear再重新绘制的思路，改成每次在不同x轴区间绘制折线并不断移动，减少了客户端的gc次数从而优化了内存使用。


## <img src="assets/tools-solid.svg" width="30px"> 技能清单

- <strong>untiy3d</strong>
- <strong>shaderlab</strong>
- <strong>.netcore</strong>
- <strong>mysql sqlserver</strong>
- <strong>react-native</strong>
- <strong>vue</strong>
- <strong>mapbox echart d3.js turf.js</strong>
- <strong>PFtrack AE Final Cut Pro</strong>

## 自我介绍
希望
