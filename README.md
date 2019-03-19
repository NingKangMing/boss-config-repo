# boss-config-repo
boss spring cloud config 系统配置中心

仓库中的配置文件会被转换成web接口，访问可以参照以下的规则：

/{application}/{profile}[/{label}]
/{application}-{profile}.yml
/{label}/{application}-{profile}.yml
/{application}-{profile}.properties
/{label}/{application}-{profile}.properties

以boss-config-dev.properties为例子，它的application是boss-config，profile是dev。client会根据填写的参数来选择读取对应的配置。
spring cloud config访问这个文件如：
http://localhost:8001/boss-config-dev.properties

访问这个文件的cloud config配置信息
http://localhost:8001/boss-config/dev
