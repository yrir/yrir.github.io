---
layout: post
title: 早早聊微前端专题分享
date: 2020-06-28 16:00:00
summary: 早早聊大会上代表飞猪分享话题<如何落地微前端一体化运营工作台>，本文为文字稿
categories: Share
---

<iframe src="https://qpluspicture.oss-cn-beijing.aliyuncs.com/vXJQN9/%E5%A6%82%E4%BD%95%E8%90%BD%E5%9C%B0%E5%BE%AE%E5%89%8D%E7%AB%AF%E4%B8%80%E4%BD%93%E5%8C%96%E8%BF%90%E8%90%A5%E5%B7%A5%E4%BD%9C%E5%8F%B0_%E4%BE%91%E5%A4%95.pdf" width="100%" height="420px" marginwidth="0" marginheight="0" scrolling="no" allowtransparency="yes"></iframe>

## 前言

大家好，我是飞猪前端侑夕，今天分享的主题是《如何落地微前端一体化运营工作台》，首先简单的介绍一下自己，花名叫做侑夕，对外网络 id 为 Tw93，目前有部分时间在弄飞猪前端技术对外影响力，运营飞猪前端团队的公众号 Fliggy F2E 以及[掘金专栏](https://juejin.im/user/55f593b160b2521fb5a02f6c/posts)，借此给大伙介绍一些飞猪前端体系化建设。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/is5qRf/微前端一体化运营工作台_侑夕.002.jpeg)

## 总览

之前 17、18、19 年分别弄的飞猪 Weex、互动、Serverless 从 0 到 1 的建设，今年 20 年主要是弄飞猪微前端一体化运营工作台的建设，也即今天分享的主题

将从「**为什么要做飞猪一体化运营工作台、要做成什么样子、怎么做的、后面想怎么做**」这 4 块来给大家讲述。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/4wIBXn/微前端一体化运营工作台_侑夕.003.jpeg)

## 为什么要做飞猪一体化运营工作台

### 飞猪运营属性的发展

在 12 年的时候，阿里 ALLIN 无线过程中，飞猪 App 当时也随之产生了，相当于工具属性，用于给用户快速查询机票门票信息；等到了 14 年左右工具属性逐步丰富起来，同时经过双十一的火爆，慢慢转变成一个营销卖货的属性，当时各种营销平台慢慢做起来了；

到了 17 年左右，当时主打场景运营心智，包括出境超市、周末好去处等主题心智，导购类平台在这个时候逐步萌芽；等到了 18 年后随着抖音/直播的火爆，飞猪运营类型也更加丰富起来了，由主题进化到内容心智。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/mfgacR/LO6Sej.png)

随着业务逐步丰富发展，内部的各种小二运营平台也在从「可用提效」往「精耕细作」发展，随着运营一体化工作台的建设，目前正处在下图箭头处

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/Uakfnw/微前端一体化运营工作台_侑夕.006.jpeg)

### 发展过程中的痛点

伴随飞猪业务的发展，我们在近两年为提升运营效率建立了多种场景的运营类平台，可满足运营完成业务诉求。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/4NVjQN/ScreenFlow.gif)

**但随着产品本身业务复杂度在不断提高，只能给运营解决温饱问题，加上各平台需要互投互通诉求逐渐强烈，在此体系下无法给业务带来 1 + 1 > 2 的价值**，面临如下继需解决的痛点：

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/qzZ7A7/微前端一体化运营工作台_侑夕.008.jpeg)

## 要做成什么样子

为解决以上痛点，我们启动一体化运营工作台建设项目，旨在借助新技术探索和升级给运营同学提供更好更高效的运营平台解决方案，一期目标为技术侧的探通，完成工作台框架的搭建，**满足多平台场景使用，沉淀一套以现有业务为基础的泛运营平台微前端解决方案**

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/f1AyW6/微前端一体化运营工作台_侑夕.009.jpeg)

基于此我们从实际业务运营配置场景入手，结合现有中后台技术和微前端解决方案，产出如下方案架构图：

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/kN3s0m/微前端一体化运营工作台_侑夕.011.jpeg)

底层借助 Ant Design 体系加上 qiankun 的能力，中间层辅助一体化工作台里面涉及的贴合现有业务场景的规范；更上一层沉淀组件化 widget 的能力，用于各种功能的互通，同时成为现有子应用的组合来源；在最上层即飞猪运营工作台的上层主应用，包括整体框架、快捷导航、权限登录控制、运营场景的汇集，包括后续要做的业务运营 SOP 解决方案。

<a href=https://qpluspicture.oss-cn-beijing.aliyuncs.com/ibXTMX/46.mp4 target="_blank"><img src=https://qpluspicture.oss-cn-beijing.aliyuncs.com/aJjkJU/23.gif width=800/></a>

## 怎么做的

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/mGaq7y/微前端一体化运营工作台_侑夕.013.jpeg)

### 前端侧深度使用共建 qiankun

在前端侧，我们深度使用和更共建 qiankun，qiankun 底层应⽤之间的加载使⽤ single-spa，上层实现样式隔离、js 沙箱、预加载等上层能⼒，同时提供[umi-plugin-qiankun](https://github.com/umijs/umi-plugin-qiankun)来解决 umi 下的快速使用，成为我们前端侧的选择方案。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/ztxsb3/微前端一体化运营工作台_侑夕.014.jpeg)

在子应用路由控制这一块，我们通过借助现有 antd pro 的路由配置，加上 qiankun 的配置项整合成一个通过的配置 config，借此对于子应用的接入只需配置此处即可，同时可以做到后面的统一管控。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/uZX8Ce/微前端一体化运营工作台_侑夕.015.jpeg)

前端侧除了微前端还有路由这一块，其实还包括可以做的更多的事情，包括我们整合了公共资源如 antd、loadsh、router 等等统一大版本，通过写了 umi-externals-url 进行处理，借此可以减少将近 1/3 的资源；包括在体验度量方面我们借助内部的能力，可以将使用用户进行分层分析包括错误性能监控；同时产出具备可以录屏、截图的在线反馈系统，便于用于在使用过程中直接反馈通知直接 issue 提交给对应的负责同学；

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/1UmnEZ/微前端一体化运营工作台_侑夕.016.jpeg)

### 后端侧自建统一网关串通主子应用

**在后端侧，我们在运营工作台 Node 侧自建了 Gateway 网关 middleware**，底层依赖[http-proxy-middleware](https://github.com/chimurai/http-proxy-middleware)能力实现，借用服务端 proxy 转发接口同时在请求上加上 token 来**解决接口登录权限以及跨域**的问题，同时对于主子应用直接接入会出现内网登录登录权限不通的问题，此处我们使用的 **免登授权** 的能力，让子应用的登录让主应用本身来提供，这样通过中间网关层配合我们给 **[qiankun pr](https://qpluspicture.oss-cn-beijing.aliyuncs.com/Z8wYlI/15.png) 的 Fetch 自定义能力和 Slave Namebase** 可解决请求和路由跳转的兼容问题。

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/R1Hiv3/微前端一体化运营工作台_侑夕.017.jpeg)

### Widget 业务组件化

微前端可以很好解决主子应用间无缝的接入问题，但是对于区块场景还不成熟，存在现有问题：

- 随着业务场景的成熟发展，加上区块能力嵌入配置的场景逐步增多；
- 借此解携抽离原有通用招造投搭能力,减少维护压力；
- 逐步丰富现有 widget 能力,满足后续更多场景的接入使用,以及系统打通

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/R0Fv6Q/JBz5nM.png)

基于此我们通过类 widget npm 组件包的方式来实现业务组件，包括制定对应的协议来驱动对应的 widget 渲染和展示，便于后端同学对其更加可控，同时在视觉规范上，我们收拢各种场景下的使用展示，便于一个 widget 可以更加无缝的嵌入到已有系统

如我们想做搭建系统里面配置互动玩法的配置，借助互动玩法配置 widget 可以达到如下的一体化配置：

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/3JCgvL/52.gif)

### 运营平台的交互体验

说到中后台的的前端侧展示，大部分场景都没有设计交互同学支持，加上一线研发同学对交互视觉标准的理解不同，**导致不少页面的使用体验勉强只能达到能用的状态，距离好看好用还有很大距离。**

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/pWdhGH/Y8twBq.png)

基于此，我们梳理几类运营场景的视觉规范需要把握的原则点：

- 同类统一：不折腾，通用层面遵循 Ant Design；同类型 / 同功能模块展示保持一致
- 舒服对齐：对齐会让页面或者强迫症的同学看起来会很舒服；标题、按钮、表单、tag 多集合类需确保对齐
- 不常用的收起：将不重要内容收起，便于让用户找关键执行点；类表格将不常用的内容隐藏或者放到抽屉里面去
- 简单不阻碍：让新用户不看说明书也可以知晓下一步操作；不能让用户由于 XXX 原因走不到下一步

比如说如下的展示：

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/2odmcP/zRTnKi.png)

通过将现有的原子类展示统一后，再往后走，我们将现有的开箱即用进行统一交互，然后沉淀出对应的能力，包括搜索列表、场景卡片组、表单预览的能力，有了这些能力的沉淀，后续新页面的产生较之前可上升一个大的阶段

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/iQQzbo/ScreenFlow.gif)

**如 FormRender 的表单的沉淀，我们可以借此此能力可以生产大量的表单页面，同时展示完全让后端侧来控制展示，这样可以做到协议驱动展示，更多详细可见 [alibaba/form-render](https://github.com/alibaba/form-render)**

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/FuX1Yk/ScreenFlow.gif)

### 后面想做啥

以上即我们第一个阶段做的事情，对于下一期重点会放在场景 SOP 能力的开发，同时在中间层进行开箱即用的疯狂提效，底层进行更多的抽象以及规范化，最底层在工程上形成统一的初始化、发布的能力

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/gy48gs/微前端一体化运营工作台_侑夕.027.jpeg)

对于运营配置的场景，最终目的是为了提升运营配置的效率以及可以不断通过数据来优化业务的使用效果，后续我们将以 SOP 的形式逐步来优化运营侧的配置，最终形成一体化的配置能力;

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/cLYF0C/微前端一体化运营工作台_侑夕.028.jpeg)

对于技术侧，将尝试更多的新技术探索，特别在微前端规范统一方面，如何让现有系统可以接入目前主流的微前端的子应用能力，包括上层子应用的管控平台；同时目前的新打包体系或许可以给我们很多新的思路来扩充现有的打包的能力；以及上述的开箱即用协议驱动的搭建如何通过低代码的搭建的方式来更多提升我们的快速生成的能力！

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/sEx6HK/微前端一体化运营工作台_侑夕.029.jpeg)

## Welcome 来飞猪

广告时间到啦，其实飞猪前端团队在阿里是一个比较厉害的前端团队，拔赤大大 P9 带队，整体成员有成熟的高 P 也有年轻的小鲜肉，大家都技术思想都很 Open，平时生日会、团队、出国 outing，不亦乐乎

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/wuu3Ff/微前端一体化运营工作台_侑夕.030.jpeg)

在技术上，目前我们在新颖技术、中台技术、基础技术上均有团队规划发展，如果你比较感兴趣，可以直接来聊，同时有能力过来带一个方向也是很欢迎的，最后也很欢迎，关注飞猪前端公众号，里面有不少体系化建设的文章干货，值得一读！

![](https://qpluspicture.oss-cn-beijing.aliyuncs.com/guQCh7/微前端一体化运营工作台_侑夕.033.jpeg)
