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

- **PowerFun Rider**

  PowerFun Rider是一款室内骑行App（PC端/移动端），用户需要拥有一台室内骑行台或者功率计连接App可以在世界地图上选择一条感兴趣的线路，在室内体验真实线路的骑行.主要功能有：单人骑行，多人赛事，影子骑行。同时集成了心率计，踏频等硬件设备（硬件协议ANT+&le）并向strava等社交平台的分享骑行数据以及相关活动页面(**vue**)

  本人在项目承担项目技术预演,后续技术分享、性能优化和任务拆分推进项目快速迭代。该项目主要经历了三个里程碑：
  
  - 1.利用**react-native**及**react-native-mapbox**实现用户头像在3D地图上按既定线路运动。

  - 2.3D骑行场景，验证**unity**版本原型并分享相关知识给小组成员。结合**mapbox for unity**插件完成第一个3D骑行场景。

  - 3.完成视频骑行或AR骑行的技术可行性验证，初步解析视频中摄像机运行轨迹并将其与unity结合，完成了国内第一个室内AR骑行的Beta版本。

  第一个里程碑我采用LayoutAnimation调用native端的动画处理，解决了动画卡顿的问题。
    - 同时在多人赛事的倒计时等计时器相关逻辑出现计时不准确的问题，同样是使用native的线程完成计时器的逻辑达到毫秒级别的同步。
    - requestAnimationFrame实现高精度计时器，提高了骑行成绩的准确性。
    - 为了节省客户端流量和电量消耗，优化蓝牙需要一直开启扫描逻辑，采用gzip算法压缩udp包大小
    - react native mapbox 部分源码，优化其地图截图文件大小，减少客户端请求体大小

  第二个里程碑解
    - chart点数过多导致渲染层卡顿甚至mesh过多问题
    - 3d地图中的线路点数过多导致绘制的mesh过多，改成可视区域内的线路显示
    - turf的distance频繁计算会导致性能下降同时将耗时的计算放到native端的线程中处理
    - 蓝牙连接问题断不开设备连不上设备扫描不到设备等，蓝牙设备的连接队列

  第三个里程碑
    学习camera solver相关技术，通过将2d视频的信息解析成3d空间信息并集合视频完后才能AR
    骑行的效果。
    通过逆向工程快速完成多人骑行避让等交互效果。
    采用循环列表完成列表卡顿的问题。
    活动页面的按需加载。
    地图优化

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
