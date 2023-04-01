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
- 电  话：152xxxx6280
- 邮  箱：anyway2019@163.com
- 微  信：lishuo710

## <img src="assets/graduation-cap-solid.svg" width="30px"> 教育经历
- 学  历：南京工业大学
- 专  业：信息与计算科学(一本)
- 其  他：CET6

## <img src="assets/briefcase-solid.svg" width="30px"> 工作经历

- #### **巨泽科技** 2019.06-至今                	     

  现在主导PowerFun系列产品研发（室内骑行、划船机App），包括后端服务开发和硬件设备对接通信（mqtt、ant+、ble），前端活动页面和管理后台，移动端混合开发。
  
  参与过事务所(高新技术企业申报项目管理类的)项目的自动化申报,国外电商类产品的前端App(react-native)与后端业务的支持。

- #### **鼎捷软件** 2017.04-2019.06                	                    
  
  独立负责部门ERP产品与PMS、WMS等系统集成，涉及到跨部门协同工作，与超过200人包(含业务、客服、客户、基础架构组)沟通，期间通过多次主动整理并复用现有或者相似集成方案，以很小的时间成本部署方案，极大提高了整个部门的产出。最终复用被纳入部门标准工作流程。

  负责大型ERP产品需求分析，整理成标准文档，并使用自研框架(客户端winform）（后端WCF)撰写日常的定制化需求。负责新人业务与技术培训并参与验收。
 

## <img src="assets/project-diagram-solid.svg" width="30px"> 项目经历

- **PowerFun**

  PowerFun Rider是一款室内骑行App（PC端/移动端），用户需要拥有一台室内骑行台或者功率计连接App可以在世界地图上选择一条感兴趣的线路，在室内体验真实线路的骑行.主要功能有：单人骑行，多人赛事，影子骑行。同时集成了心率计，踏频等硬件设备（硬件协议ANT+&le）并向strava等社交平台的分享骑行数据以及相关活动页面(**vue**)

  我在PowerFun Rider项目中承担了项目技术预演的责任，并推动了项目的快速迭代。该项目实现了室内骑行的App，细分功能包括单人骑行、多人赛事、影子骑行等。项目主要使用了PC端和移动端的技术，并需要用户拥有室内骑行台或功率计连接App，以在世界地图上选择感兴趣的线路，实现室内体验真实线路的骑行。

  整个项目主要经历了三个里程碑，每个里程碑都有着相应的技术难点和解决方案。在第一个里程碑中，我采用LayoutAnimation调用native端的动画处理，解决了动画卡顿的问题，并使用 native 的线程完成计时器的逻辑，提高了骑行成绩的准确性。为了节省客户端流量和电量消耗，我还优化了蓝牙连接部分，采用gzip算法压缩udp包大小，减少了客户端请求体大小。

  在第二个里程碑中，我遇到了chart点数过多、3d地图中线路点数过多等问题，导致渲染层卡顿或mesh过多问题，我通过改成可视区域内的线路显示，将性能得到了极大的提升。同时，我还将耗时的计算放到native端的线程中处理，实现了更好的性能表现。另外，我还优化了蓝牙连接部分，解决了设备连不上设备、扫描不到设备等问题。

  第三个里程碑是实现视频骑行或AR骑行的技术可行性验证，初步解析视频中摄像机运行轨迹并将其与unity结合，完成了国内第一个室内AR骑行的Beta版本。相应的技术难点包括学习camera solver相关技术，通过逆向工程快速完成多人骑行避让等交互效果，采用循环列表完成列表卡顿的问题和活动页面的按需加载。整个项目的三个里程碑都是承担了项目技术预演的责任，并通过技术解决方案推动项目的快速迭代和发展。

  用requetanimation 结合perfmance。Now构建前端高精度定时器用来渲染人物头像的移动
  利用原生线程完成逻定时器作为后端定时器完成逻辑层的数据采集，既保证了数据的准确性也保证了前端动画的流畅度（  解决了因为定时器不准导致的人物移动动画的抖动问题）

  untiy中我们遇到了有些线路过长导致绘制的LineRender占用了大量的内存和渲染压力，实现可视区域内线路的动态加载，解决长线路（超过100km）渲染卡顿问题，同时内存占用从原来的1g以上优化到 450MB左右。同时从数据层面滤波算法减少海拔误差，并且两点之间的坡度做了线性插值使得线路的波动趋于平滑大大提高了用户骑行体验。

  对于线路相关数据采用本地缓存同时通过etag来确保本地数据的实时性，减少了线路数据的网络请求。

  对于运动相关的数据比较耗费cpu的数据转移到客户端减少了服务器cpu会100%的问题，导致服务器卡顿的问题。

  修改mapbox的native端源码的优化图片质量的优化已经相关手势功能完成业务需要。

  前端vue活动页面的map和chart组件按需加载优化了pc端的cef或者移动端webview打开活动页面白屏时间长的问题。

  实现了Powerfun独有的风格的Button等独有控件集合，并且使用栈结构实现了轻量的客户端页面路由，实现了轻量化的多语言切换功能。实现了高精度计时器，循环列表，对象池，日期同步，佛历，波斯历，本地化数据等同步等一些列扩展方法或者工具，为后续开发提供了很大的方便，同事之需要关注业务细节。

  在实际开过程中持续做检查性能，优化了一些不合理的code，比如unity chart插件使用的优化，将Chart动态绘制曲线clear再重新绘制的方式改为动态移动x轴并在不同区间绘制实时曲线，不可见部分的内存占用由unity和chart插件本身的剔除机制在合适的时机释放这样避免了因频繁clear而导致频繁gc引发性能问题。

  自学unity shader PFtrack等视频处理程序解析到3d空间数据圆满完成unity ar相关的业务需求，实现了国内首个室内AR骑行的产品,目前已经发布Beta版本。

  主动集成App Center用于监控前端异常（包括偶发的闪退，硬件通讯异常，android或ios版本兼容性等问题),及时定位线上问题并上报。


## <img src="assets/tools-solid.svg" width="30px"> 技能清单

- <strong>untiy3d</strong>
- <strong>shaderlab</strong>
- <strong>.netcore</strong>
- <strong>mysql sqlserver</strong>
- <strong>react-native</strong>
- <strong>vue</strong>
- <strong>mapbox echart d3.js turf.js</strong>
- <strong>PFtrack AE Final Cut Pro</strong>
