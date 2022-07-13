# buession-springboot-boot 参考手册


[SpringBoot](https://spring.io/projects/spring-boot) 基础库依赖，封装 SpringBoot Application 启动抽象类，封装 SpringBoot Banner 抽象类。


---


### **安装**

```xml
<dependency>
    <groupId>com.buession.springboot</groupId>
    <artifactId>buession-springboot-boot</artifactId>
    <version>x.x.x</version>
</dependency>
```

该模块定义了 SpringBootApplication 的接口，简化了您的 SpringBootApplication 启动类的创建(更多的使用方式，将在[buession-springboot-web](2.0/web/index.md)和[buession-springboot-cli](2.0/cli/index.md)讲解)。该模块还将自动自动配置 `MessagePropertyBeanPostProcessor`。


## [API 参考手册>>](/manual/2.0/docs/buession-springboot-boot/)