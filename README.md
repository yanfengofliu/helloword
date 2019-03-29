# helloword
第一个厂库项目描述

### springboot打war包在tomcat中运行

首先main方法类继承SpringBootServletInitializer类重写configure（）方法
```
@Override
    protected SpringApplicationBuilder configure(SpringApplicationBuilder builder) {
        return builder.sources(DemoApplocation.class);
    }
```
然后再pol.xml中添加插件,注意标注<packeging>war</packeging>
```
 <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-tomcat</artifactId>
            <scope>provided</scope>
        </dependency>
        
  <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
```
