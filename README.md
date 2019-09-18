# springcloud项目搭建

### 1.1 使用sprngboot创建一个父类工程不添加任何的依赖

  运行CloudApplication 项目组正常运行commit

### 1.2 父类工程修改pom.xml

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

### 1.3 父类工程添加一个common module(其他子模块都依赖当前的模块)

  运行CloudApplication 项目组正常运行commit

### 1.4 common module修改pom.xml

```xml
    <parent>
            <groupId>cloud</groupId>
            <artifactId>cloud</artifactId>
            <version>0.0.1-SNAPSHOT</version>
       </parent>      
    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
        <java.version>1.8</java.version>
        <spring-cloud.version>Finchley.SR1</spring-cloud.version>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-redis</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-bus-amqp</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-aop</artifactId>
        </dependency>

        <dependency>
            <groupId>org.apache.tomcat.embed</groupId>
            <artifactId>tomcat-embed-core</artifactId>
        </dependency>
        <dependency>
            <groupId>com.google.guava</groupId>
            <artifactId>guava</artifactId>
            <version>${guava-version}</version>
        </dependency>
        <dependency>
            <groupId>io.jsonwebtoken</groupId>
            <artifactId>jjwt</artifactId>
            <version>${jjwt-version}</version>
        </dependency>
        <dependency>
            <groupId>io.springfox</groupId>
            <artifactId>springfox-swagger2</artifactId>
            <version>${swagger.version}</version>
        </dependency>
        <dependency>
            <groupId>io.springfox</groupId>
            <artifactId>springfox-swagger-ui</artifactId>
            <version>${swagger.version}</version>
        </dependency>
        <dependency>
            <groupId>com.google.code.gson</groupId>
            <artifactId>gson</artifactId>
            <version>${gson.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.security</groupId>
            <artifactId>spring-security-core</artifactId>
            <version>${spring.serurity.version}</version>
        </dependency>
        <dependency>
            <groupId>com.baomidou</groupId>
            <artifactId>mybatis-plus-core</artifactId>
            <version>3.0.1</version>
            <scope>compile</scope>
        </dependency>
        <dependency>
            <groupId>com.baomidou</groupId>
            <artifactId>mybatis-plus-extension</artifactId>
            <version>3.0.1</version>
            <scope>compile</scope>
        </dependency>
    </dependencies>



```

子类的配置文件正常映入 CloudApplication运行正常