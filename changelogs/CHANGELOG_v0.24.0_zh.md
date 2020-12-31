# Changelog

本文档记录了 0.24 中协作、开发、部署、测试以及平台管理等功能的增加、优化和BUG修复记录。

# 基础功能

### [0.24.0] - 2020-12-31

## 新增功能

* 平台管理与组织管理的安全策略中新增强制用户修改默认密码的设置；
* 组织层与项目层的自定义角色新增支持删除的功能；
* 工作台-快速链接中新增置顶功能，支持将任意链接置顶；
* 工作台-快速链接中新增个人分组，支持单独查看项目或个人的快速链接；
* 项目层新增客户端的创建与管理功能，并支持项目所有者在此为客户端分配项目角色；

## 功能优化

* 优化了用户创建失败后的操作，此时支持停用此用户；

## 缺陷修复

* 修复了平台层任务管理页面，点击浏览器刷新时白屏的问题；
* 修复了LDAP同步记录中同步类型显示的问题；
* 修复了登录Token失效后多标签页弹框的问题；
* 修复了工作台中，偶现最近使用环境重复出现的问题；
* 修复了消息铃铛通知中，流水线的跳转链接有误且点击后报错的问题；
* 修复了项目层-通知-资源删除验证，勾选某个框之后，点击保存，勾选的内容无效的问题；

# 敏捷协作 

### [0.24.0] - 2020-12-31

## 新增功能

* 支持关注问题项；
* 新增甘特图功能，以便项目管理员进行任务排期；
* 工作列表问题项支持批量删除；
* 问题项支持关联或新建测试用例；
* 故事地图新增冲刺泳道；
* 故事地图支持所有字段进行筛选；
* 看板支持一键折叠、一键展开；
* 新增绩效，通过图表展示冲刺的完成情况，以便更好的管理项目；
### 绩效功能

分析当前冲刺故事、任务、缺陷情况及历史冲刺故事、任务、缺陷趋势变化，以便用户更好的了解冲刺的完成情况。

* 故事点分布图从计划、实际两个维度展示故事点、任务工时主要负责人的数量以及占比；
* 故事完成情况图从故事点、任务两个维度展示主要负责人计划、实际完成对比及百分比；
* 缺陷排行榜从非生产环境、生产环境两个维度展示责任人、创建人缺陷数量并按降序排列；
* 缺陷分布图从非生产环境、生产环境两个维度展示责任人、创建人缺陷数量柱状分布图；
* 问题完成趋势图从故事点、任务工时两个维度展示每个冲刺计划、完成数量及顺冲刺的变化；
* 缺陷趋势分析图从非生产环境、生产环境两个维度展示责任人、创建人每个冲刺缺陷数量及随冲刺的变化，可通过责任人筛选；
## 功能优化

* 优化故事地图卡片样式；
* 优化看板卡片样式；
* 优化状态机自定义流转；
* 优化问题详情剩余问题显示；
* 优化问题复制时同时复制自定义字段的值；
* 优化搜索栏支持全选、反选、无；
## 缺陷修复

* 禁用点击空白关闭弹窗；

# 代码开发 

### [0.24.0] - 2020-12-31

## 新增功能

* 流水线-代码检查任务中新增Maven单测的功能；
* 流水线CD阶段中新增外部卡点的任务，用于触发外部的工作流或其他系统；
* 应用服务版本新增支持批量删除的功能；
## 功能优化

* 优化了应用流水线树结构中的搜索，直接筛出含有字段的对象，并进行字体颜色加深；
* 创建与修改流水线的界面新增通过拖拽来改变阶段与任务的顺序；
* 优化了流水线页面的刷新加载速度；
## 缺陷修复

* 修复了创建流水线，添加任务时，应用服务为空问题；
* 修复了流水线中人工卡点任务，可以选择没有应用服务权限的成员作为审核人员的问题；
* 修复了应用流水线-CD阶段-部署任务中，不支持修改配置信息的问题；
* 修复了实例视图中，共享应用服务详情中信息的展示问题；

# 环境部署 

### [0.24.0] - 2020-12-31

## 新增功能

* 部署模块新增主机配置功能，支持项目人员在此维护管理部署类型的主机；
* 手动部署模块新增主机部署的方式，支持将jar包与Docker镜像直接部署到已有的主机中；
* 集群模块新增“新建集群”的操作，支持通过录入节点来新建集群；
* 集群模块新增支持增减“平台集群”的节点，并支持移除节点中的master或etcd角色；
## 功能优化

* 针对同一集群下的service外部ip及端口，添加了不能重复的限制；
## 缺陷修复

* 修复了部署配置页面列表中各个字段排序报错的问题；

# 测试管理

### [0.24.0] - 2020-12-31

## 新增功能

* 测试计划新增测试报告；

# 制品库

### [0.24.0] - 2020-12-31

## 新增功能

* 新增maven、npm制品仓库删除功能；
* 新增组织时创建harbor仓库；
* 制品库中允许有的项目所有者都能在Nexus仓库中给自己或项目成员分配角色；
* 制品库中允许所有Nexus仓库人员都能看到Nexus制品库下载记录；

## 缺陷修复

* harbor初始化脚本空指针修复；
* saga任务扫描不到修复；

 