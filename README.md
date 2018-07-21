# AgileBPM 敏捷工作流开发平台

#### 项目介绍

项目部署、实施文档 请参考 http://doc.agilebpm.cn/  

PC在线测试地址 http://test.agilebpm.cn/login.html

[功能缺陷提测](http://zentao.agilebpm.cn账号test密码test123456)

![移动端测试地址](https://images.gitee.com/uploads/images/2018/0719/100556_de9bc8a4_1861740.png "屏幕截图.png")
移动端测试 账号密码 admin 1

## 工作流解决方案
**我们通过业务对象、表单、流程引擎共同协作来解决业务流难实施的痛点**

业务对象用来承载、持久化业务数据；表单则是业务数据的展示层；流程则用来驱动业务数据流转。

三者协作完成流程实施。

> 
- **业务对象:**  由实体（表）组成，支持任意数据结构（关联关系），可以跨库来组织业务对象（支持分布式事务）。而且难以置信的支持N层。
- **业务表单:**  表单完美的支撑了业务对象的展示，并支持丰富的前端组件和字段级权限控制。
- **流程引擎:**  高效、解耦、强大、灵活。流程引擎**一切功能皆插件**。

**支持任意结构的业务对象 + 丰富控件易扩展的表单（字段级别的权限控制）  + 功能强大的工作流引擎** 
便是我们完整的流程解决方案

当然、流程也支持url表单，方便已有业务、异构系统的流程实施

**具体实施步骤请参考 [文档](https://agile-bpm.gitee.io/docs/implement/businessObject.html) 中的敏捷流程实施三部曲** :smirk: 
> 流程配置页面、任务处理页面、流程实例页面截图

<img src="https://images.gitee.com/uploads/images/2018/0719/110744_34dddb3b_1861740.png" width="33%" hegiht="300" align=left /> 
<img src="https://images.gitee.com/uploads/images/2018/0719/110900_7f2d6a78_1861740.png" width="33%" hegiht="300" align=left /> 
<img src="https://images.gitee.com/uploads/images/2018/0719/111013_03f9b51c_1861740.png" width="33%" hegiht="300" align=left /> 
> 流程表单界面截图

## 软件架构说明

#### 组件化
系统通过功能划分出了多个模块，每个模块由API、CORE、REST、SERVICE(apiImpl) 几部分组成。模块与模块间通过API交互，WEB则用于整合各个模块 

[系统模块介绍介绍]( http://agilebpm.gitee.io/docs/base/framework.html)

[组件更多详细介绍](http://agilebpm.gitee.io/docs/base/module.html)
 

#### 前后端分离
AgileBPM 是一个前后端分离的项目，这样各个团队会更专注于其本职工作，后端只负责业务逻辑、API 提供。而大前端则不拘泥于一种前端技术、更自由的构建UI交互逻辑

#### 项目技术组件
![项目组件](https://images.gitee.com/uploads/images/2018/0705/172349_e5de827a_1861740.png "屏幕截图.png")


##### 其他项目中用到的组件
前端：bootstrap-table，codemirror，echarts，layer，markdown，softable，ueditor，ztree
移动端：vue，vux,weui

#### 架构模式
AgileBPM 目前是标准的SOA架构，但依然拥有微服务架构的特点。
可以通过选择WEB模块的依赖来构建您需要的服务模块，然后修改API 实现，选择一个服务注册中心，就完成了微服务的改造

我们建议业务前期使用AgileBPM的这种模块化管理的架构模式，运维实施陈本小，也不必关注分布式事务问题，业务后期也可以很轻易的向微服务架构迁移。

## 系统功能
- 资源管理： 用于服务器鉴权，用户分配资源菜单
- 数据字典： 定义业务字段的可选项 如：证件类型
- 定时计划： 定时调度引擎
- 系统属性： 多环境系统参数定义
- 系统数据源： 系统支持多数据源的数据获取，系统数据源的动态切换，读写数据源的分离
- 工作台：个人自定义首页
- 流水号
- 常用脚本
- 自定义对话框
- 系统树： 用于系统分类

流程、组织、表单、鉴权模块功能这里不介绍。


## 其他说明
我们是专业工作流研发团队，有多年工作流程实施经验，针对各种特殊场景，经过近一年多的(业余)时间设计开发了这款产品。
目前还有很多组件正在筹备开发中，如果有更多人支持，我们也会继续下去。

## 目前基础版源码正在整理中......
qq 交流群 477781857