文档：
	[阿里云百炼-官方文档地址](https://help.aliyun.com/zh/model-studio/application-user-guide/?spm=a2c4g.11186623.help-menu-2400256.d_1.6e922562Fapzxs&scm=20140722.H_2840916._.OR_help-T_cn~zh-V_1)
	[Spring-Ai-Alibaba文档](https://java2ai.com/docs/1.0.0-M6.1/get-started/?spm=5176.29160081.0.0.2c69aa5cwWQo6O)

1. 创建获取Api Key : [https://bailian.console.aliyun.com/?tab=model#/api-key](https://bailian.console.aliyun.com/?tab=model#/api-key)
2. 创建应用获取appId
3. 引入依赖
```xml
<!--阿里AI-->  
<dependency>  
	<groupId>com.alibaba.cloud.ai</groupId>  
	<artifactId>spring-ai-alibaba-starter</artifactId>  
	<version>1.0.0-M5.1</version>  
</dependency>
```
注意： 如果是项目升级的话 一定要确认好 spring-cloud-alibaba-dependencies 的版本 要不会出现下方问题
[![](https://czx-dev.github.io/2025/03/07/ai/%E6%8E%A5%E5%85%A5%E9%98%BF%E9%87%8C%E4%BA%91%E7%99%BE%E7%82%BC/845b98c7f475db956ac30f6fb1b4c23.png)](https://czx-dev.github.io/2025/03/07/ai/%E6%8E%A5%E5%85%A5%E9%98%BF%E9%87%8C%E4%BA%91%E7%99%BE%E7%82%BC/845b98c7f475db956ac30f6fb1b4c23.png)
4. 配置文件
```yml
spring:  
	ai:  
		dashscope:  
			agent:  
				app-id: ##########  
#尚方获取的api_key 注意空间  
			api-key: *********  
			chat:  
				options:  
#模型名称  
					model: qwen-max
```