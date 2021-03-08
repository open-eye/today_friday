### Test

先是确定表字段，基本的增删改查，登陆。创建流程文件，创建流程引擎，加载流程定义，部署流程

### activiti 的表

1. act_ge_ 通用数据表，ge是general的缩写
2. act_hi_ 历史数据表，hi是history的缩写，对应HistoryService接口
3. act_id_ 身份数据表，id是identity的缩写，对应IdentityService接口
4. act_re_ 流程存储表，re是repository的缩写，对应RepositoryService接口，存储流程部署和流程定义等静态数据
5. act_ru_ 运行时数据表，ru是runtime的缩写，对应RuntimeService接口和TaskService接口，存储流程实例和用户任务等动态数据



### 自己的表

角色表 sys_role

角色权限表 sys_role_permission

角色用户表 sys_user_role

权限表 sys_permission

type 菜单，权限，菜单与权限，

![image-20210302102203635](C:\Users\THINK\Documents\MyFiles\myBlog\mdFiles\Test.assets\image-20210302102203635.png)

用户表 employee

上级id，角色id，salt



Activiti

Activity是模型时期对象（想想BPMN文件的那些元素），它有3个子类：CallActivity, SubProcess, Task（注意是

+ org.activiti.bpmn.model.Task）

流程启动的那个活动可以理解成有一个StartEventActivity

Task有N个子类：BusinessRuleTask, ManualTask, ReceiveTask, ScriptTask, SendTask, ServiceTask, UserTask

PvmActivity是部署时期对象，ActivityImpl是它的实现类，注意ActivityImpl与Activity没有关系！



Activiti 执行流程

![image-20210303155805253](C:\Users\THINK\Documents\MyFiles\myBlog\mdFiles\Test.assets\image-20210303155805253.png)



发布流程，选择压缩包，点击发布，请求后台，controller层调用service层方法，service层调用repositoryService，根据压缩包部署流程，会保存到数据库

查看我的代办事务



查看我的报销单

