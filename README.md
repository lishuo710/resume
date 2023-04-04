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
  
  #### 项目概述：

  该App是一款结合骑行台等设备进行室内骑行的App,拥有单人骑行、多人赛事、影子骑行等功能，并集成了心率计、踏频等硬件设备，支持向社交平台分享骑行数据和一系列活动页面。

  我作为项目小组组长，负责技术方案预演，保证项目迭代进度和持续性能优化。该项目共分为三个里程碑，每个里程碑都有着相应的技术难点和解决方案。

  #### <strong>技术解决方案：</strong>

  - 第一阶段：在第一个里程碑中，早期我们已经由了基于WPF结合CEF的PC端App,我们团队根据既有场景，采用react-native结合react native mapbox开发第一个移动端App。

  - 第二阶段：第二阶段，根据业务需求已经react-native在webgl结合多人联机等复杂的业务场景下用户体验和性能表现瓶颈的情况下，决定采用unity3d结合unity-mapbox完成更加真实的3D骑行。

  - 第三阶段：在现有unity版本的基础上为了实现AR骑行，我了解AR相关的技术，并成功验证了CG相关技术和unity3d结合迭代出第一版本基于Video的AR骑行。

  #### <strong>技术实现细节：</strong>
  - 我采用LayoutAnimation调用native端的动画处理，解决了动画卡顿的问题，并使用 native 的线程完成计时器的逻辑，提高了骑行成绩的准确性。同时优化了蓝牙连接部分，采用gzip算法压缩udp包大小，减少了客户端请求体大小。
  - 利用requetanimation 结合performance.now构建前端高精度定时器，实现头像的移动；
  - 前端定时器与后端定时器共同完成数据采集和处理，确保数据准确性和动画流畅性；
  - 将超长线路（超过100km）的LineRender改为可视区域内的动态加载，减少内存占用和渲染压力；
  - 采用滤波算法减少海拔误差，并对两点之间的坡度做线性插值，提高用户骑行体验；
  - 在unity版本中出现了LineRender占用大量内存和渲染压力问题，改为可视区域内线路的动态加载，解决了渲染卡顿问题；优化了蓝牙连接部分，解决了设备连不上设备、扫描不到设备等问题。
  - 在验证AR技术的阶段，我通过解析视频中摄像机运行轨迹并将其与unity结合，完成了国内首个室内AR骑行的Beta版本。优化了性能表现和嵌入平台功能，包括学习camera solver相关技术，通过逆向工程快速完成多人骑行避让等交互效果，采用循环列表完成列表卡顿的问题和活动页面按需加载等技术难点。
  - 采用本地缓存并使用ETag确保本地数据的实时性，减少线路数据（gps&海拔等文件）的网络请求；
  - 计算运动相关的数据转移到客户端，减轻服务器的CPU计算压力，并解决因用户并发上传数据可能会导致100%的问题；
  - 实现 Powerfun 独有的控件集合，并使用栈结构实现轻量的客户端页面路由，实现轻量化的多语言切换功能；
  - 集成 App Center 用于监控前端异常并及时定位并上报。

  #### <strong>其他贡献：</strong>

   - 持续做性能优化，优化了一些不合理的代码，如采用根据可视区域内线路的动态绘制曲线；使用Chart动态移动x轴并在不同区间绘制实时曲线等技术。自学 Unity shader PFtrack 等视频处理程序，解析到3d空间数据，圆满完成 Unity AR 相关的业务需求，实现了国内首个室内AR骑行的产品，目前已经发布Beta版本。

  #### <strong>项目效益：</strong>

   - PowerFun Rider 达成了项目预期和目标，完成了室内骑行的 App 的开发和推广；通过技术解决方案的推动，进行了快速的迭代和发展，提高了产品的质量和用户体验。同时在现有技术方案下完成另外一款室内划船机的app，通过原有的技术积累快速迭代并顺利上线。


## <img src="assets/tools-solid.svg" width="30px"> 技能清单

- <strong>untiy3d</strong>
- <strong>shaderlab</strong>
- <strong>.netcore</strong>
- <strong>mysql sqlserver</strong>
- <strong>react-native</strong>
- <strong>vue</strong>
- <strong>mapbox echart d3.js turf.js</strong>
- <strong>PFtrack AE Final Cut Pro</strong>
