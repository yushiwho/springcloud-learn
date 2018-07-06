# tips
* eureka做UT时，可以暂时关闭，在test/resources中添加application.yml文件，配置如下
```yml
eureka:
  client:
    enabled: false
```
* 微服务内存不足时考虑设置jvm的参数大小，eureka server可以设置为128m，网关256m，业务虚拟机根据情况，开发测试时可设置为128m
```
java -Xmx 128m -Xms 128m -jar your.jar
```
* intellij在Edit configuration->configuration->vm options中设置