# Redis

Redis是一个开源，基于内存的高性能key-Value数据库，它支持存储的value类型很丰富，包括string(字符串)、list(链表)、set(集合)、zset(sortedset--有序集合)和hash（哈希类型）。

本镜像源自于DockerHub镜像[tutum/redis](https://registry.hub.docker.com/u/tutum/redis/)。


## 说明

容器启动后，会默认生成一个随机密码，你可以通过查看容器日志获得密码，比如


	========================================================================
	You can now connect to this Redis server using:

	    redis-cli -a iuiouljwi9tjw5638u65lkj6356 -h <host> -p <port>

	Please remember to change the above password as soon as possible!
	========================================================================

在上面的例子中，*iuiouljwi9tjw5638u65lkj6356* 就是随机密码。

如果你想设置一个特定的密码，你可以设置环境变量 *REDIS_PASS* 为您需要的密码。

如果你想启动Redis并忽略密码登录，你可以设置环境变量 *REDIS_PASS* 为 \*\*None\*\*。

## 配置Redis

如果你想设置Redis的配置，你可以把配置加*REDIS_*前缀作为一个环境变量传入容器中，例如您想设置tcp-keepalive为60，可以设置环境变量REDIS_TCP_KEEPALIVE=60

