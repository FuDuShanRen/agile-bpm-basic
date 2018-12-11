#### 选择数据库类型，按SQL顺序依次执行 create 脚本、init 脚本
#### 当有版本升级时，请执行 upgrade 升级脚本
#### 请忽略changesql,该文件仅仅在更新快照版本时才有用，为内部开发使用脚本

## 也可以选择需要的模块来安装需要的sql

#### **sys** 系统模块 18 张表

含 常用脚本、流水号、子系统、菜单资源、通用授权、首页面板、系统属性、数据字典、附件上传等功能表  

#### **org** 组织模块 7 张表

含 组织、岗位、用户、角色、职务 

#### **bus-form** 业务表单模块 共 9 张表

含业务表、业务对象、业务字段、表单、自定义对话框等信息

#### **wf** 流程模块 共  20 张表 ， AgileBPM包装的 7 张表，以及 Activiti 原生用到的  13 张表

含act流程定义表、act流程运行时表、ab流程意见、ab流程运行堆栈记录、ab流程任务表、ab候选人表、ab业务数据关联表

## mysql 版本必须5.6以上（因为系统用到了分区表，版本太低不支持）