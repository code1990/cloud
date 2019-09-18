# springcloud项目搭建

### 1.1 使用sprngboot创建一个父类工程不添加任何的依赖

  运行CloudApplication 项目组正常运行commit

### 1.2 父类工程添加如下的配置文件

```xml
    <properties>
        <spring-cloud.version>Finchley.SR1</spring-cloud.version>
        <guava-version>20.0</guava-version>
        <jjwt-version>0.9.0</jjwt-version>
        <mybatis-plus-starter.version>3.0.1</mybatis-plus-starter.version>
        <mysql-connector.version>5.1.46</mysql-connector.version>
        <swagger.version>2.9.2</swagger.version>
        <gson.version>2.8.2</gson.version>
        <spring.serurity.version>5.0.8.RELEASE</spring.serurity.version>
        <qcloudsms.version>1.0.5</qcloudsms.version>
    </properties>
    
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.springframework.cloud</groupId>
                <artifactId>spring-cloud-dependencies</artifactId>
                <version>${spring-cloud.version}</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>

```

运行CloudApplication 项目组正常运行