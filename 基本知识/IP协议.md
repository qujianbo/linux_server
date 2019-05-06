#IP协议
##IP服务的特点
- 无连接
	通信双方都不长久地维持对方的任何信息。这样，上层协议每次发数据的时候，都必须明确指定对方的IP。
- 无状态
	无法处理乱序和重复的数据报。
- 不可靠
	是指IP协议不能保证IP数据报准确地到达接收端，多种情况会导致发送失败
##IP模块的工作流程
![IP工作流程](https://github.com/qujianbo/linux_server/blob/master/img/IP%E5%B7%A5%E4%BD%9C%E6%B5%81%E7%A8%8B.PNG)
##路由表
![](https://github.com/qujianbo/linux_server/blob/master/img/%E8%B7%AF%E7%94%B1%E8%A1%A8%E5%AE%9E%E4%BE%8B.PNG)
![](https://github.com/qujianbo/linux_server/blob/master/img/%E8%B7%AF%E7%94%B1%E8%A1%A8%E5%86%85%E5%AE%B9.PNG)
### 路由表机制 ###
1. 查找路由表中和数据包的目标IP地址完全匹配的主机IP地址。如果找到，就使用该路由项，没找到则转步骤2
2. 查找路由表中和数据包的目标IP地址具有相同网路ID的网络IP地址，如果找到，就使用该路由项：没找到则转步骤3
3. 选择默认路由项，这通常意味着数据报的下一跳路由是网关

这里只挑出一些个人觉得需要注意的内容，关于IP协议其他的比如字段什么的我就不赘述了。