<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Linkis 安装及使用指南](#linkis-%E5%AE%89%E8%A3%85%E5%8F%8A%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%97)
  - [1. 背景](#1-%E8%83%8C%E6%99%AF)
  - [2. 简介](#2-%E7%AE%80%E4%BB%8B)
    - [2.1 Linkis](#21-linkis)
      - [2.1.1 核心特性](#211-%E6%A0%B8%E5%BF%83%E7%89%B9%E6%80%A7)
    - [2.2 DataSphereStudio](#22-dataspherestudio)
  - [3. 安装](#3-%E5%AE%89%E8%A3%85)
    - [3.1 涉及组件版本说明](#31-%E6%B6%89%E5%8F%8A%E7%BB%84%E4%BB%B6%E7%89%88%E6%9C%AC%E8%AF%B4%E6%98%8E)
    - [3.2 依赖环境安装](#32-%E4%BE%9D%E8%B5%96%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85)
    - [3.3 安装包准备](#33-%E5%AE%89%E8%A3%85%E5%8C%85%E5%87%86%E5%A4%87)
    - [3.4 安装](#34-%E5%AE%89%E8%A3%85)
      - [3.4.1 安装环境检查](#341-%E5%AE%89%E8%A3%85%E7%8E%AF%E5%A2%83%E6%A3%80%E6%9F%A5)
        - [3.4.1.1 硬件环境检查](#3411-%E7%A1%AC%E4%BB%B6%E7%8E%AF%E5%A2%83%E6%A3%80%E6%9F%A5)
        - [3.4.1.2 依赖环境检查](#3412-%E4%BE%9D%E8%B5%96%E7%8E%AF%E5%A2%83%E6%A3%80%E6%9F%A5)
        - [3.4.1.3 安装用户检查](#3413-%E5%AE%89%E8%A3%85%E7%94%A8%E6%88%B7%E6%A3%80%E6%9F%A5)
        - [3.4.1.4 安装命令检查](#3414-%E5%AE%89%E8%A3%85%E5%91%BD%E4%BB%A4%E6%A3%80%E6%9F%A5)
        - [3.4.1.5 目录检查](#3415-%E7%9B%AE%E5%BD%95%E6%A3%80%E6%9F%A5)
      - [3.4.2 解压安装包](#342-%E8%A7%A3%E5%8E%8B%E5%AE%89%E8%A3%85%E5%8C%85)
      - [3.4.3 修改配置](#343-%E4%BF%AE%E6%94%B9%E9%85%8D%E7%BD%AE)
      - [3.4.4 安装目录与配置检查](#344-%E5%AE%89%E8%A3%85%E7%9B%AE%E5%BD%95%E4%B8%8E%E9%85%8D%E7%BD%AE%E6%A3%80%E6%9F%A5)
      - [3.4.5 启动服务](#345-%E5%90%AF%E5%8A%A8%E6%9C%8D%E5%8A%A1)
      - [3.4.6 功能测试](#346-%E5%8A%9F%E8%83%BD%E6%B5%8B%E8%AF%95)
        - [3.4.6.1 Hive](#3461-hive)
        - [3.4.6.2 Spark](#3462-spark)
        - [3.4.6.3 UDF 函数](#3463-udf-%E5%87%BD%E6%95%B0)
        - [3.4.6.4 Linkis 调试方式](#3464-linkis-%E8%B0%83%E8%AF%95%E6%96%B9%E5%BC%8F)
          - [3.4.6.4.1 客户端方式](#34641-%E5%AE%A2%E6%88%B7%E7%AB%AF%E6%96%B9%E5%BC%8F)
          - [3.4.6.4.2 SDK 方式](#34642-sdk-%E6%96%B9%E5%BC%8F)
    - [3.5 扩展功能](#35-%E6%89%A9%E5%B1%95%E5%8A%9F%E8%83%BD)
      - [3.5.1 Hive 支持 TEZ 引擎](#351-hive-%E6%94%AF%E6%8C%81-tez-%E5%BC%95%E6%93%8E)
        - [3.5.1.1 Linkis 操作](#3511-linkis-%E6%93%8D%E4%BD%9C)
        - [3.5.1.2 本地集群配置](#3512-%E6%9C%AC%E5%9C%B0%E9%9B%86%E7%BE%A4%E9%85%8D%E7%BD%AE)
          - [3.5.1.2.1 container 模式](#35121-container-%E6%A8%A1%E5%BC%8F)
          - [3.5.1.2.2 llap 模式](#35122-llap-%E6%A8%A1%E5%BC%8F)
        - [3.5.1.3 Linkis 脚本测试](#3513-linkis-%E8%84%9A%E6%9C%AC%E6%B5%8B%E8%AF%95)
      - [3.5.2 Flink 引擎支持](#352-flink-%E5%BC%95%E6%93%8E%E6%94%AF%E6%8C%81)
        - [3.5.2.1 本地安装 Flink](#3521-%E6%9C%AC%E5%9C%B0%E5%AE%89%E8%A3%85-flink)
        - [3.5.2.2 新增 Flink 引擎插件](#3522-%E6%96%B0%E5%A2%9E-flink-%E5%BC%95%E6%93%8E%E6%8F%92%E4%BB%B6)
        - [3.5.2.3 Flink Connector 调试](#3523-flink-connector-%E8%B0%83%E8%AF%95)
          - [3.5.2.3.1 Kafka Connector](#35231-kafka-connector)
          - [3.5.2.3.2 Mysql Connector](#35232-mysql-connector)
          - [3.5.2.3.3 Mysql CDC Connector](#35233-mysql-cdc-connector)
          - [3.5.2.3.4 Elasticsearch Connector](#35234-elasticsearch-connector)
        - [3.5.2.4 自定义开发 Connector](#3524-%E8%87%AA%E5%AE%9A%E4%B9%89%E5%BC%80%E5%8F%91-connector)
          - [3.5.2.4.1 Redis Connector](#35241-redis-connector)
          - [3.5.2.4.2 MongoDB Connector](#35242-mongodb-connector)
        - [3.5.2.5 提交 Flink 作业](#3525-%E6%8F%90%E4%BA%A4-flink-%E4%BD%9C%E4%B8%9A)
  - [4. 最佳实践](#4-%E6%9C%80%E4%BD%B3%E5%AE%9E%E8%B7%B5)
    - [4.1 Hive](#41-hive)
      - [4.1.1 权限不足导致引擎启动失败](#411-%E6%9D%83%E9%99%90%E4%B8%8D%E8%B6%B3%E5%AF%BC%E8%87%B4%E5%BC%95%E6%93%8E%E5%90%AF%E5%8A%A8%E5%A4%B1%E8%B4%A5)
      - [4.1.2 Container exited with a non-zero exit code 1](#412-container-exited-with-a-non-zero-exit-code-1)
      - [4.1.3 NoSuchMethodError](#413-nosuchmethoderror)
      - [4.1.4 No LLAP Daemons are running](#414-no-llap-daemons-are-running)
    - [4.2 Spark](#42-spark)
      - [4.2.1 ClassNotFoundException](#421-classnotfoundexception)
      - [4.2.2 ClassCastException](#422-classcastexception)
    - [4.3 Flink](#43-flink)
      - [4.3.1 method did not exist](#431-method-did-not-exist)
  - [5. 参考](#5-%E5%8F%82%E8%80%83)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Linkis 安装及使用指南

本文主要用于指导用户进行 **[Linkis](https://github.com/WeBankFinTech/Linkis)**
及 **[DataSphereStudio](https://github.com/WeBankFinTech/DataSphereStudio)** 的安装、部署， 以及对 Scriptis 功能中 Hive、Spark、Flink
引擎脚本的测试，以便用户可以快速入手 Linkis 和 认识其核心功能。对于其数据交换、数据服务、数据质量、任务调度等功能未做测试，可以结合官方文档进行安装、测试。

## 1. 背景

公司自主研发的大数据中台产品，用以帮助用户快速收集数据、整理数据、构建数仓、数据服务以及数据资产管理。其中涉及很多大数据组件，各个组件都有各自的
API，导致开发者学习成本较高，也不易于维护。故考虑抽离出计算层，负责对接上层应用，连接大数据底层存储、计算引擎的工作也由计算层统一处理，而 Linkis
提供了这种能力，打通了多个计算存储引擎（如：Spark、Flink、Hive、Python等），对外提供统一 REST/WebSocket/JDBC 接口，故安装 Linkis，对其核心 功能进行测试。

## 2. 简介

### 2.1 Linkis

Linkis 作为上层应用程序和底层引擎之间的计算中间件，通过使用 Linkis 提供的 REST/WebSocket/JDBC 等标准接口，上层应用可以方便地连接访问 MySQL/Spark/Hive/Presto/Flink
等底层引擎，同时实现变量、脚本、函数和资源文件等用户资源的跨上层应用互通。 作为计算中间件，Linkis 提供了强大的连通、复用、编排、扩展和治理管控能力。
通过计算中间件将应用层和引擎层解耦，简化了复杂的网络调用关系，降低了整体复杂度，同时节约了整体开发和维护成本。

2021 年 8 月 2 日，微众银行开源项目 [Linkis](https://incubator.apache.org/clutch/linkis.html) 正式通过国际顶级开源组织 Apache 软件基金会（简称 ASF
）的投票决议，以全票通过的优秀表现成为 ASF 孵化器项目。

#### 2.1.1 核心特性

- **丰富的底层计算存储引擎支持**。  
  **目前支持的计算存储引擎**：Spark、Hive、Python、Presto、ElasticSearch、MLSQL、TiSpark、JDBC、Shell、Flink 等。
  **支持的脚本语言**：SparkSQL, HiveQL, Python, Shell, Pyspark, R, Scala、JDBC 等。
- **强大的计算治理能力**。基于 Orchestrator、Label Manager 和定制的 Spring Cloud Gateway 等服务，Linkis 能够提供基于多级标签的跨集群/跨 IDC
  细粒度路由、负载均衡、多租户、流量控制、资源控制和编排策略(如双活、主备等)支持能力。
- **全栈计算存储引擎架构支持**。能够接收、执行和管理针对各种计算存储引擎的任务和请求，包括离线批量任务、交互式查询任务、实时流式任务和存储型任务。
- **资源管理能力**。 ResourceManager 不仅具备对 Yarn 和 Linkis EngineManager 的资源管理能力，还将提供基于标签的多级资源分配和回收能力，让 ResourceManager
  具备跨集群、跨计算资源类型的强大资源管理能力。
- **统一上下文服务**。为每个计算任务生成 context id，跨用户、系统、计算引擎的关联管理用户和系统资源文件（ JAR、ZIP、Properties 等），结果集，参数变量，函数等，一处设置，处处自动引用。
- **统一物料**。系统和用户级物料管理，可分享和流转，跨用户、系统共享物料。

### 2.2 DataSphereStudio

DataSphereStudio（以下简称 DSS ）是微众银行自研的数据应用开发管理集成框架。基于插拔式的集成框架设计，及计算中间件 Linkis ，可轻松接入上层各种数据应用系统，让数据开发变得简洁又易用。在统一的 UI 下，
DataSphereStudio 以工作流式的图形化拖拽开发体验，将满足从数据交换、脱敏清洗、分析挖掘、质量检测、可视化展现、定时调度到数据输出应用等，数据应用开发全流程场景需求。

> DSS 集成度极高，目前已集成的系统有：

- 数据开发IDE工具——[Scriptis](https://github.com/WeBankFinTech/Scriptis)

- 数据可视化工具——[Visualis](https://github.com/WeBankFinTech/Visualis)

- 数据质量管理工具——[Qualitis](https://github.com/WeBankFinTech/Qualitis)

- 工作流调度工具——[Schedulis](https://github.com/WeBankFinTech/Schedulis)

- 数据交换工具——[Exchangis](https://github.com/WeBankFinTech/Exchangis)

- 数据Api服务——[DataApiService](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/zh_CN/%E4%BD%BF%E7%94%A8%E6%96%87%E6%A1%A3/DataApiService%E4%BD%BF%E7%94%A8%E6%96%87%E6%A1%A3.md)

- 流式应用开发管理工具——[Streamis](https://github.com/WeBankFinTech/Streamis)

## 3. 安装

本文安装、测试采用的 Linkis 版本为 1.0.2、DSS 版本为
1.0.0，由于安装时尚在内测阶段，故直接使用 [DSS1.0 + Linkis1.0.2一键部署包](https://osp-1257653870.cos.ap-guangzhou.myqcloud.com/WeDatasphere/DataSphereStudio/1.0.0-RC1/DSS-Linkis%E5%85%A8%E5%AE%B6%E6%A1%B620210817.zip)
，可直接点击下载安装。此部署包主要包括 Scriptis（数据开发面板） 和 管理台（引擎、微服务管理及全局历史日志）。对于可视化、数据质量、工作流调度、数据交换、数据服务等功能，可以自行参照官方文档安装，本文不再赘述。

本文安装涉及到的组件有 Hadoop、Hive、Spark、Flink，关于此环境的相关 JAR 包也会放到网盘，包括（Hive 对 TEZ 引擎的支持、Spark 对 Hive 的支持、Flink 对各种
Connector 的支持）。另外， Hive 引擎、Flink 引擎的 lib 目录下的 JAR 包，也会上传作为参考，有部分问题是由于 JAR 包的缺少或版本问题导致。

```
链接：https://pan.baidu.com/s/17g05rtfE_JSt93Du9TXVug 
提取码：zpep

 计算层
    ├─Linkis引擎 #linkis引擎插件压缩包
    │      flink_engine.zip
    │      hive_engine.zip #支持tez
    │      spark_engine.zip
    └─本地集群 #本地集群配置及JAR包
    │       flink_linkis.zip
    │       hive_linkis.zip
    │       spark_linkis.zip
    └─udf #自定义函数测试JAR包
            hive_udf.jar
            flink_udf.jar
```

安装过程遇到问题，可以先查阅官方 Q&A，记录了安装、使用过程中常见问题，地址为：https://docs.qq.com/doc/DSGZhdnpMV3lTUUxq

由于仅为功能性测试，本文安装 DSS 及 Linkis
都是单机版，并未多活、多副本部署。若要多节点部署，可以参考官方文档 **[Cluster_Deployment](https://github.com/WeBankFinTech/Linkis-Doc/blob/master/zh_CN/Deployment_Documents/Cluster_Deployment.md)**

### 3.1 涉及组件版本说明

![版本说明](https://upload-images.jianshu.io/upload_images/12555001-5fb69d3aa8b720be.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

由于我们集群组件版本和 Linkis 默认支持的引擎组件版本有差异，故需要自行编译相应插件。需要下载 Linkis 源码，修改相应组件版本，重新编译。

### 3.2 依赖环境安装

Linkis 作为计算中间件，自身元数据的存储需要依赖 Mysql，而一些计算、存储引擎则是根据我们的需要安装。本文主要使用 Hive、Spark、Flink 引擎，其中 Flink 引擎 又会涉及到
Kafka、Redis、MongoDB、Elasticsearch 等组件。在安装 Linkis 之前，应该确保这些组件已经安装完成，且可以正常使用。本文测试依赖的集群为非安全集群， 未启用 Kerberos 认证。

其中，Spark 官网安装包并无 Hive 的支持，需要自行编译 Spark，以支持 Hive。需正确指定 Hadoop 版本、Scala 版本及加入 Hive 支持，需保证本地可以成功运行 SparkSQL。

理论上，安装 Linkis 的服务器只需要和安装以上服务的服务器保证网络互通即可。

### 3.3 安装包准备

可以使用 [DSS1.0 + Linkis1.0.2一键部署包](https://osp-1257653870.cos.ap-guangzhou.myqcloud.com/WeDatasphere/DataSphereStudio/1.0.0-RC1/DSS-Linkis%E5%85%A8%E5%AE%B6%E6%A1%B620210817.zip)
进行安装，但是由于 Linkis 引擎插件 版本不一致，需要全局更改相应组件版本，重新编译 Linkis。且在 1.0.2 版本，Flink
引擎虽然已经支持，但是在编译的时候，不会加入到安装包中，需要单独编译，以增加新插件的方式加入，之后也会做详细说明。

以下是编译命令：

```shell
// 首次拉取代码,需要执行以下命令,完成初始化
mvn -N install
// 执行打包命令
mvn clean install -Dmaven.test.skip=true
```

### 3.4 安装

#### 3.4.1 安装环境检查

Linkis 在正式安装之前，需要做一些准备工作：

- 硬件环境检查主要保证微服务可以正常启动，不会由于资源不足，无法正常启动。

- 依赖环境检查主要保证 Linkis 启动可以正常使用，避免无法执行命令导致脚本执行失败。

- 安装用户检查主要检查安装用户是否存在及配置相应权限，Linkis 支持指定提交、执行用户。

- 安装命令检查主要保证可以顺利安装，安装过程中会使用到一些命令。需提前检查，保证顺利安装。

- 目录检查主要保证 Linkis 配置的缓存目录存在，避免执行过程找不到目录。

##### 3.4.1.1 硬件环境检查

默认每个微服务 JVM 堆内存为 512 M，可以通过修改 `SERVER_HEAP_SIZE` 来统一调整每个微服务的堆内存，如果服务器资源较少，建议修改该参数为 128 M。如下：

```bash
    vim ${LINKIS_HOME}/config/linkis-env.sh
```

```bash
    # java application default jvm memory.
    export SERVER_HEAP_SIZE="128M"
```

安装 DSS 和 Linkis 服务，共会启动 6 个 DSS 的微服务，及 8 个 Linkis 的微服务，当 Linkis 执行 Hive、Spark、Flink 等任务时，还会启动 `LINKIS-CG-ENGINECONN`
微服务， 采用单机版安装，需要保证所有微服务可以全部启动。

##### 3.4.1.2 依赖环境检查

> **Hadoop 环境：** 需要配置了`HADOOP_HOME`、`HADOOP_CONF_DIR`环境变量，且这两个目录存在。且在安装 Linkis 的服务器上可以执行`hadoop fs -ls /`命令。

> **Hive 环境：** 需要配置了`HIVE_HOME`、`HIVE_CONF_DIR`环境变量，且这两个目录存在。若无法读取到 Hive 配置文件，可能出现无法正常获取元数据信息，会使用内置的 Derby 作为 Hive 的元数据库。

> **Spark 环境：** 需要配置了`SPARK_HOME`、`SPARK_CONF_DIR`环境变量，且这两个目录存在，需要保证安装 Spark 引擎插件的服务器上可以执行`spark-submit --version`命令，Spark 的任务会通过这个命令提交到 YARN 上执行。为了保证 SparkSQL 对 Hive 的支持，除了保证成功在本地运行`spark-sql`命令，还需要保证 SparkSQL on YARN 模式也可以成功执行。具体命令为`./spark-sql --master yarn --deploy-mode client`，在客户端中测试 SQL 任务。

> **Flink 环境：** 需要配置了`FLINK_HOME`、`FLINK_CONF_DIR`、`FLINK_LIB_DIR`环境变量，且这三个目录存在。

建议直接拷贝`Hadoop`、`Hive`、`Spark`、`Flink`目录及子目录到相应的节点，并配置环境变量，环境变量修改完毕后，需要使其生效，命令`source /etc/profile`，环境变量参考如下：

```
export JAVA_HOME=/opt/jdk1.8
export CLASSPATH=.$CLASSPATH:$JAVA_HOME/lib
export HADOOP_HOME=/opt/install/hadoop
export HADOOP_CONF_DIR=$HADOOP_HOME/etc/hadoop
export HIVE_HOME=/opt/install/hive
export HIVE_CONF_DIR=$HIVE_HOME/conf
export FLINK_HOME=/opt/install/flink
export FLINK_CONF_DIR=/opt/install/flink/conf
export FLINK_LIB_DIR=/opt/install/flink/lib
export SPARK_HOME=/opt/install/spark
export SPARK_CONF_DIR=$SPARK_HOME/conf
export PATH=$MAVEN_HOME/bin:$HADOOP_HOME/bin:$HIVE_HOME/bin:$SPARK_HOME/bin:$SQOOP_HOME/bin/:$FLINK_HOME/bin:$FLINKX_HOME/bin:$JAVA_HOME/bin:$PATH
export CLASSPATH=.$CLASSPATH:$JAVA_HOME/lib
```

检查环境变量是否生效：

```shell
sudo su - ${username}
echo ${JAVA_HOME}
echo ${FLINK_HOME}
```

> **Mysql 环境：** 由于 Linkis 使用 Mysql 保存元数据，且使用的查询语法与 Mysql 的默认配置不兼容，会出现`ONLY_FULL_GROUP_BY`的报错，需要修改 `sql_mode`。另外在 Flink 引擎的测试中，需要开启 Mysql binlog，在环境检查的时候，一并做修改。若用不到开启 binlog，也可以不做修改。

i. 修改 `sql_mode` 配置：

```
1. 查看当前的sql_mode
select @@global.sql_mode;
2. 修改sql_mode
vim /etc/my.cnf
sql_mode=STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION
3. 重启 Mysql 服务
service mysqld restart
service mysqld status
```

ii. 开启 binlog

```
1. 修改配置 vim /etc/my.cnf，增加以下配置
   server_id=1
   log_bin=mysql-bin
   binlog_format=ROW
   expire_logs_days=30
2. 重启 Mysql 服务
service mysqld restart
service mysqld status
3. 查看状态
show VARIABLES LIKE 'log_bin';
show global variables like "binlog%";
```

##### 3.4.1.3 安装用户检查

例如: **部署用户是 hadoop 账号**

> 先查看系统中是否已经有 hadoop 用户，搭建完集群，hadoop 用户可能已经存在，若已经存在，则直接授权即可；若不存在，先创建用户，再授权。

- 查看是否存在 hadoop 用户，命令为：`cat /etc/passwd | grep hadoop`

```
httpfs:x:983:976:Hadoop HTTPFS:/var/lib/hadoop-httpfs:/bin/bash
mapred:x:982:975:Hadoop MapReduce:/var/lib/hadoop-mapreduce:/bin/bash
kms:x:979:972:Hadoop KMS:/var/lib/hadoop-kms:/bin/bash
```

- 若不存在，则创建 hadoop 用户，并加入 hadoop 用户组，命令为：`sudo useradd hadoop -g hadoop`

- 给 hadoop 用户授权 sudo 权限，命令为：`vi /etc/sudoers`，在文件中添加`hadoop  ALL=(ALL)       NOPASSWD: NOPASSWD: ALL`内容，由于文件是只读的，使用`wq!`
  强制保存即可

- 修改安装用户的环境变量,`vim /home/hadoop/.bash_rc`配置环境变量，环境变量如下：

```
export JAVA_HOME=/opt/jdk1.8
export HADOOP_HOME=/opt/install/hadoop
export HADOOP_CONF_DIR=/opt/install/hadoop/etc/hadoop
export HIVE_HOME=/opt/install/hive
export HIVE_CONF_DIR=/opt/install/hive/conf
export FLINK_HOME=/opt/install/flink
export FLINK_CONF_DIR=/opt/install/flink/conf
export FLINK_LIB_DIR=/opt/install/flink/lib
export SPARK_HOME=/opt/install/spark
export SPARK_CONF_DIR=/opt/install/spark/conf
```

##### 3.4.1.4 安装命令检查

Linkis 需要的命令工具（在正式安装前，脚本会自动检测这些命令是否可用，如果不存在会尝试自动安装，安装失败则需用户手动安装以下基础 shell 命令工具）：

* telnet
* tar
* sed
* dos2unix
* yum
* java
* unzip
* expect

可以查看`vim bin/checkEnv.sh`脚本中检查的命令，对于某些不需要的功能的命令检查，可以注释掉。如：python 命令的检查等。

##### 3.4.1.5 目录检查

Linkis 服务需要用户配置本地引擎目录`ENGINECONN_ROOT_PATH`和日志缓存目录`HDFS_USER_ROOT_PATH`，可以选择将日志缓存到 HDFS 上，也可以缓存到本地，如果配置了 HDFS
路径，会默认将日志及执行结果写入 HDFS。

> `ENGINECONN_ROOT_PATH`为本地目录，需要用户提前创建，并且完成授权，授权命令`chmod -R 777 /目录`，若为 Linkis1.0.2 版本，不必提前创建与授权，会在脚本、程序中自动创建与授权。

> `HDFS_USER_ROOT_PATH`为 HDFS 上的路径，需要提前创建，且完成授权，授权命令`hadoop fs -chmod -R 777 /目录`。

#### 3.4.2 解压安装包

使用`unzip`命令解压，其中包括 linkis、dss、web的安装包，每个组件也有各自的安装、配置脚本。总体原则是根据需要修改 conf 目录下的配置文件，若配置修改完成，可以使用 bin 目录下的安装、启动脚本完成安装、启动操作。
用户可以使用一键 install 命令，进行一键安装，也可以自行解压各个压缩包，自行安装。使用一键安装，可能会出现统一配置未同步到 linkis、dss、web等组件中，需要在启动前认真检查。

解压目录如下：

```
│  wedatasphere-dss-1.0.0-dist.tar.gz #dss后端安装包，使用一键install命令，会自动解压
│  wedatasphere-dss-web-1.0.0-dist.zip #web前端安装包，使用一键install命令，会自动解压
│  wedatasphere-linkis-1.0.2-combined-package-dist.tar.gz #linkis后端安装包，使用一键install命令，会自动解压 
│
├─bin
│      checkEnv.sh #安装前命令检查脚本，不需要的命令，可以注释跳过检查
│      install.sh #一键安装命令，会完成解压、创建必须目录、导入元数据等操作
│      replace.sh #内部使用脚本，用于完成统一配置的覆盖
│      start-all.sh #一键启动所有微服务脚本，先启动linkis，再启动dss后端，再启动dss前端
│      stop-all.sh #一键停止所有微服务脚本
│
└─conf
        config.sh #统一配置脚本，会通过replace.sh脚本，将配置分别覆盖到各组件的各个微服务中
        db.sh #统一数据库配置脚本，包括linkis元数据库配置、hive元数据库配置
```

#### 3.4.3 修改配置

用户需要在`conf/db.sh`配置 Linkis、Hive 的元数据库连接信息，在`conf/config.sh`脚本中配置 DSS、Linkis
安装、启动的信息。由于存在十几个微服务，所以在配置微服务端口号的时候，需要格外注意，避免端口号被占用。

查看端口号占用情况：

```shell
# 查看所有端口号
netstat -ntlp
# 查看当前是否被占用
netstat -tunlp |grep  8080
```

db.sh 配置示例：

```properties
## for DSS-Server and Eventchecker APPJOINT
MYSQL_HOST=host
MYSQL_PORT=port
MYSQL_DB=db
MYSQL_USER=user
MYSQL_PASSWORD=password
##hive的配置
HIVE_HOST=host
HIVE_PORT=port
HIVE_DB=db
HIVE_USER=user
HIVE_PASSWORD=password
```

config.sh 配置示例：

```properties
### deploy user
deployUser=hadoop
### Linkis_VERSION
LINKIS_VERSION=1.0.2
### DSS Web
DSS_NGINX_IP=127.0.0.1
DSS_WEB_PORT=8088
### DSS VERSION
DSS_VERSION=1.0.0
############## ############## linkis的其他默认配置信息 start ############## ##############
### Generally local directory
WORKSPACE_USER_ROOT_PATH=file:///tmp/linkis/ 
### User's root hdfs path
HDFS_USER_ROOT_PATH=hdfs:///tmp/linkis 
### Path to store job ResultSet:file or hdfs path
RESULT_SET_ROOT_PATH=hdfs:///tmp/linkis 
### Path to store started engines and engine logs, must be local
ENGINECONN_ROOT_PATH=/appcom/tmp
### 引擎环境变量配置
HADOOP_CONF_DIR=/opt/install/hadoop/etc/hadoop
HIVE_CONF_DIR=/opt/install/hive/conf
SPARK_CONF_DIR=/opt/install/spark/conf
##YARN REST URL  spark engine required
YARN_RESTFUL_URL=http://127.0.0.1:8088
### for install
LINKIS_PUBLIC_MODULE=lib/linkis-commons/public-module
## 微服务端口配置
###  You can access it in your browser at the address below:http://${EUREKA_INSTALL_IP}:${EUREKA_PORT}
#LINKIS_EUREKA_INSTALL_IP=127.0.0.1         # Microservices Service Registration Discovery Center
LINKIS_EUREKA_PORT=20303
###  Gateway install information
#LINKIS_GATEWAY_PORT =127.0.0.1
LINKIS_GATEWAY_PORT=8001
### ApplicationManager
#LINKIS_MANAGER_INSTALL_IP=127.0.0.1
LINKIS_MANAGER_PORT=8101
### EngineManager
#LINKIS_ENGINECONNMANAGER_INSTALL_IP=127.0.0.1
LINKIS_ENGINECONNMANAGER_PORT=8102
### EnginePluginServer
#LINKIS_ENGINECONN_PLUGIN_SERVER_INSTALL_IP=127.0.0.1
LINKIS_ENGINECONN_PLUGIN_SERVER_PORT=8103
### LinkisEntrance
#LINKIS_ENTRANCE_INSTALL_IP=127.0.0.1
LINKIS_ENTRANCE_PORT=8104
###  publicservice
#LINKIS_PUBLICSERVICE_INSTALL_IP=127.0.0.1
LINKIS_PUBLICSERVICE_PORT=8105
### cs
#LINKIS_CS_INSTALL_IP=127.0.0.1
LINKIS_CS_PORT=8108
########## Linkis微服务配置完毕##### 
################### The install Configuration of all DataSphereStudio's Micro-Services #####################
# 用于存储发布到 Schedulis 的临时ZIP包文件
WDS_SCHEDULER_PATH=file:///appcom/tmp/wds/scheduler
### This service is used to provide dss-framework-project-server capability.
#DSS_FRAMEWORK_PROJECT_SERVER_INSTALL_IP=127.0.0.1
DSS_FRAMEWORK_PROJECT_SERVER_PORT=9007
### This service is used to provide dss-framework-orchestrator-server capability.
#DSS_FRAMEWORK_ORCHESTRATOR_SERVER_INSTALL_IP=127.0.0.1
DSS_FRAMEWORK_ORCHESTRATOR_SERVER_PORT=9003
### This service is used to provide dss-apiservice-server capability.
#DSS_APISERVICE_SERVER_INSTALL_IP=127.0.0.1
DSS_APISERVICE_SERVER_PORT=9004
### This service is used to provide dss-workflow-server capability.
#DSS_WORKFLOW_SERVER_INSTALL_IP=127.0.0.1
DSS_WORKFLOW_SERVER_PORT=9005
### dss-flow-Execution-Entrance
### This service is used to provide flow execution capability.
#DSS_FLOW_EXECUTION_SERVER_INSTALL_IP=127.0.0.1
DSS_FLOW_EXECUTION_SERVER_PORT=9006
### This service is used to provide dss-datapipe-server capability.
#DSS_DATAPIPE_SERVER_INSTALL_IP=127.0.0.1
DSS_DATAPIPE_SERVER_PORT=9008
########## DSS微服务配置完毕#####
############## ############## other default configuration 其他默认配置信息  ############## ##############
## java application minimum jvm memory
export SERVER_HEAP_SIZE="128M"
##sendemail配置，只影响DSS工作流中发邮件功能
EMAIL_HOST=smtp.163.com
EMAIL_PORT=25
EMAIL_USERNAME=xxx@163.com
EMAIL_PASSWORD=xxxxx
EMAIL_PROTOCOL=smtp
```

#### 3.4.4 安装目录与配置检查

**i. 安装**

修改完配置，使用一键安装命令`bin/install.sh`，完成安装。

安装完成后，会生成 linkis、dss、web三个目录，以下列出每个目录的目录树，只展示主要目录。

linkis 目录树如下：

```
├── linkis
│   ├── bin #主要存放linkis功能相关的命令，如客户端执行hive、spark任务等
│   │   ├── linkis-cli
│   │   ├── linkis-cli-hive
│   │   ├── linkis-cli-spark-sql
│   │   ├── linkis-cli-spark-submit
│   │   └── linkis-cli-start
│   ├── conf #linkis微服务的配置文件
│   │   ├── application-eureka.yml
│   │   ├── application-linkis.yml
│   │   ├── linkis-cg-engineconnmanager.properties
│   │   ├── linkis-cg-engineplugin.properties
│   │   ├── linkis-cg-entrance.properties
│   │   ├── linkis-cg-linkismanager.properties
│   │   ├── linkis-cli
│   │   │   ├── linkis-cli.properties
│   │   │   └── log4j2.xml
│   │   ├── linkis-env.sh
│   │   ├── linkis-mg-gateway.properties
│   │   ├── linkis.properties
│   │   ├── linkis-ps-cs.properties
│   │   ├── linkis-ps-publicservice.properties
│   │   ├── log4j2.xml
│   │   └── token.properties
│   ├── db #linkis元数据初始化的sql脚本
│   │   ├── linkis_ddl.sql
│   │   ├── linkis_dml.sql
│   ├── lib #linkis各个模块的依赖包
│   │   ├── linkis-commons
│   │   ├── linkis-computation-governance
│   │   │   ├── linkis-cg-engineconnmanager
│   │   │   ├── linkis-cg-engineplugin
│   │   │   ├── linkis-cg-entrance
│   │   │   ├── linkis-cg-linkismanager
│   │   │   └── linkis-client
│   │   │       └── linkis-cli
│   │   ├── linkis-engineconn-plugins
│   │   │   ├── appconn
│   │   │   ├── flink
│   │   │   ├── hive
│   │   │   ├── python
│   │   │   ├── shell
│   │   │   └── spark
│   │   ├── linkis-public-enhancements
│   │   │   ├── linkis-ps-cs
│   │   │   └── linkis-ps-publicservice
│   │   └── linkis-spring-cloud-services
│   │       ├── linkis-mg-eureka
│   │       └── linkis-mg-gateway
│   ├── LICENSE
│   ├── README_CN.md
│   ├── README.md
│   └── sbin #linkis启动脚本，用于启动各个微服务
│       ├── common.sh
│       ├── ext
│       │   ├── linkis-cg-engineconnmanager
│       │   ├── linkis-cg-engineplugin
│       │   ├── linkis-cg-entrance
│       │   ├── linkis-cg-linkismanager
│       │   ├── linkis-common-start
│       │   ├── linkis-mg-eureka
│       │   ├── linkis-mg-gateway
│       │   ├── linkis-ps-cs
│       │   └── linkis-ps-publicservice
│       ├── linkis-daemon.sh
│       ├── linkis-start-all.sh
│       └── linkis-stop-all.sh
```

dss 目录树如下：

```
├── dss
│   ├── bin #dss安装脚本目录
│   │   ├── appconn-install.sh
│   │   ├── checkEnv.sh
│   │   ├── excecuteSQL.sh
│   │   └── install.sh
│   ├── conf #dss各个微服务配置目录
│   │   ├── application-dss.yml
│   │   ├── config.sh
│   │   ├── db.sh
│   │   ├── dss-apiservice-server.properties
│   │   ├── dss-datapipe-server.properties
│   │   ├── dss-flow-execution-server.properties
│   │   ├── dss-framework-orchestrator-server.properties
│   │   ├── dss-framework-project-server.properties
│   │   ├── dss.properties
│   │   ├── dss-workflow-server.properties
│   │   ├── log4j2.xml
│   │   ├── log4j.properties
│   │   └── token.properties
│   ├── dss-appconns #dss集成其它系统存放目录，如可视化、数据质量、调度等
│   ├── lib #dss各个微服务依赖包
│   ├── README.md
│   └── sbin #dss微服务启动脚本目录，支持一键启动、单个启动
│       ├── common.sh
│       ├── dss-daemon.sh
│       ├── dss-start-all.sh
│       ├── dss-stop-all.sh
│       └── ext
│           ├── dss-apiservice-server
│           ├── dss-datapipe-server
│           ├── dss-flow-execution-server
│           ├── dss-framework-orchestrator-server
│           ├── dss-framework-project-server
│           └── dss-workflow-server
```

web 目录树如下：

```
├── web
│   ├── config.sh #web前端的配置脚本，如gateway地址等
│   ├── dist #dss前端静态文件
│   ├── dss #linkis前端静态文件(管理台是由linkis集成进来)
│   │   └── linkis
│   └── install.sh #安装启动脚本，安装、配置nginx
```

**ii. 检查配置**

> **配置检查：** 使用一键安装命令安装完成后，有些配置未完全覆盖，需要用户自行检查，确保配置正确。以下是安装过程中碰到的问题：

```
1. dss中gateway地址配置错误，修改dss.properties配置文件，正确配置gateway地址
2. web中config.sh脚本中，gateway地址配置错误，需用户自行修改
3. linkis1.0.2中引擎目录会在创建引擎前完成自动授权，需要开启代理。修改linkis-cg-engineconnmanager.properties，添加wds.linkis.storage.enable.io.proxy=true
```

#### 3.4.5 启动服务

**i. 启动服务**

完成安装与配置检查步骤后，有两种方式启动微服务：

一种是使用一键启动脚本`bin/start-all.sh`来启动所有微服务，包括 linkis 后端、dss后端、web前端。

另一种方式是进入到各自的安装目录， 自行启动所有微服务，先启动 linkis 服务，使用`linkis/sbin/linkis-start-all.sh`命令即可，当然对于 linkis 服务，也可以单独进行各微服务的启停。再启动 dss
服务，使用`dss/sbin/dss-start-all.sh`命令。 最后启动 web 服务，使用`web/install.sh`，会自动检查是否安装
nginx，若没有，会自动下载安装，并完成配置。另外需要注意，`web/install.sh`脚本配置 ngnix 是覆盖的方式，若一台服务器上需要启动多个 web 服务，配置 多个 nginx 监听，那么需要自行修改脚本，以免 ngnix
配置被覆盖掉。

**ii. 查看是否启动成功**

可以在 Eureka 界面查看 Linkis & DSS 后台各微服务的启动情况。未执行任务的情况下，Linkis 共 8 个微服务，DSS 共 6 个 微服务；当有 Scriptis 任务执行的时候，Linkis
会启动 `LINKIS-CG-ENGINECONN` 服务。以下给出默认微服务的日志目录：

```
// 1. linkis 微服务日志目录，默认启动的 8 个微服务的日志都在这里，具体可以对应查看每个微服务的日志
linkis/logs
// 2. linkis 引擎微服务的日志，需要参考 `ENGINECONN_ROOT_PATH` 获取引擎的根目录。一般情况下，若引擎未成功启动，需要关注 `linkis-cg-engineconnmanager` 日志；若启动成功，需要关注引擎日志；若引擎启动成功，任务执行失败，可以先查看引擎日志，若无具体信息，可以查看 YARN 日志，查看具体报错。
${ENGINECONN_ROOT_PATH}/hadoop/workDir/UUID/logs
// 3. dss 微服务日志，默认启动的 6 个微服务日志都在这里，具体可以对应查看每个微服务日志
dss/logs
// 4. 前端问题可以打开调试，查看具体请求，根据请求获取具体哪个微服务接口问题，再根据以上目录，查看具体微服务的日志
```

Eureka 微服务界面：

![dss-微服务](https://upload-images.jianshu.io/upload_images/12555001-945cf74ace840c6e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![linkis-微服务](https://upload-images.jianshu.io/upload_images/12555001-7185c82e1a08ba70.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**iii. 谷歌浏览器访问**

请使用谷歌浏览器访问以下前端地址：`http://DSS_NGINX_IP:DSS_WEB_PORT` 启动日志会打印此访问地址。登陆时管理员的用户名和密码均为部署用户名，如部署用户为hadoop，则管理员的
用户名/密码为：hadoop/hadoop。

可以在 `linkis-mg-gateway.properties` 配置中配置 LDAP 信息，接入内部 LDAP 服务。

基于 DSS1.0试用版，很多功能做了限制：

- 登录页面，首页会展示主要功能面板及案例；

![首页](https://upload-images.jianshu.io/upload_images/12555001-3434a82562326ded.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- Scriptis 面板是我们此次安装、测试的重点，用于编写 Hive、Spark、Flink等脚本及函数的管理；

![Scriptis](https://upload-images.jianshu.io/upload_images/12555001-8bf12c7f12c84b62.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 管理台为 linkis 前台界面集成进来的，主要包括全局历史（脚本执行日志）、资源管理（引擎资源的使用情况，当有引擎启动的时候才会展示）、参数配置（yarn 资源队列、引擎资源配置等）、全局变量（全局变量配置）、ECM管理（ECM
  实例管理，也可对 ECM 下的引擎进行管理）、微服务管理（微服务管理面板）

![管理台](https://upload-images.jianshu.io/upload_images/12555001-4d346d11926ffe3b.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 3.4.6 功能测试

本文主要对 Hive、Spark、Flink引擎进行测试，默认安装的 Linkis 并未集成 Flink 引擎，故先对 Hive、Spark引擎测试。另外，对于自定义函数也进行了测试。

在使用过程中，遇到的一些报错及解决方案，也会在下文 **[最佳实践](#4-%E6%9C%80%E4%BD%B3%E5%AE%9E%E8%B7%B5)** 中指出。遇到报错，可以参考 **[最佳实践](#4-%E6%9C%80%E4%BD%B3%E5%AE%9E%E8%B7%B5)**。

##### 3.4.6.1 Hive

**i. Hive 配置文件**

Hive 连接器支持多种计算引擎，如 MR、TEZ、Spark等，默认使用 MR 引擎，需要在 `hive-site.xml` 中指定，本文配置为测试使用，并未做优化，仅供参考：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
    <property>
        <name>hive.metastore.schema.verification</name>
        <value>false</value>
    </property>
    <property>
        <name>hive.metastore.uris</name>
        <value>thrift://host:9083</value>
    </property>
    <property>
        <name>spark.master</name>
        <value>yarn-cluster</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionURL</name>
        <value>jdbc:mysql://host:3306/hive</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionDriverName</name>
        <value>com.mysql.cj.jdbc.Driver</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionUserName</name>
        <value>root</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionPassword</name>
        <value>MySQL5.7</value>
    </property>
    <property>
        <name>hive.auto.convert.join</name>
        <value>false</value>
        <description>Enables the optimization about converting common join into mapjoin</description>
    </property>
</configuration>
```

**ii. 脚本测试**

在 Scriptis 面板新建脚本，脚本类型选择 hive 即可。脚本测试需要稍微复杂点的 SQL，避免 Hive 解析，只走本地查询，并未启动 MR 任务，脚本参考：

```sql
show
tables;
select name, addr, id
from linkis_1
group by name, addr, id
order by id;
select a.name, a.addr, b.phone
from linkis_1 a
         left join linkis_2 b on a.id = b.id
group by a.name, a.addr, b.phone
order by a.name;
```

**iii. 基准测试**

若需要基准测试，可以参考 **[hive-testbench](https://github.com/hortonworks/hive-testbench)** 基准测试框架进行测试，此框架提供了基于 TPC-DS 和 TPC-H
基准测试的数据生成器和示例查询， TPC-DS 采用星型、雪花型等多维数据模式。它包含 7 张事实表，17 张纬度表平均每张表含有 18 列。其工作负载包含 99 个 SQL 查询，覆盖 SQL99 和 2003 的核心部分以及 OLAP。
这个测试集包含对大数据集的统计、报表生成、联机查询、数据挖掘等复杂应用，测试用的数据和值是有倾斜的，与真实数据一致。TPC-DS 作为客观衡量多个不同 Hadoop 版本以及 SQL on Hadoop 技术的最佳测试集。
这个基准测试有以下几个主要特点：

* 共 99 个测试案例，遵循 SQL99 和 SQL 2003 的语法标准，SQL 案例比较复杂
* 分析的数据量大，并且测试案例是在回答真实的商业问题
* 测试案例中包含各种业务模型（如分析报告型，迭代式的联机分析型，数据挖掘型等）
* 几乎所有的测试案例都有很高的 IO 负载和 CPU 计算需求

##### 3.4.6.2 Spark

Linkis 对于 Spark Engineconn Plugin 的支持，基本无需更改，主要问题在于：一是编译 Spark 插件，选择与 Spark 集群环境相同的 Scala 版本、JDK 版本等；二是 Spark
集群环境的正确配置，若是在本地可以正确执行以下步骤，一般 Linkis 插件也可以正确执行。

**i. 本地测试**

```
// 1. 确保spakr作业可以成功提交，测试命令如下：

./spark-submit \
--class org.apache.spark.examples.SparkPi \
--master yarn \
--executor-memory 1G \
--total-executor-cores 2 \
/opt/install/spark/examples/jars/spark-examples_2.11-2.4.3.jar \
100

// 2. 确保spark on hive，且为yarn模式可以成功执行。默认启动是本地模式，只要本地有hive的依赖就可以成功，yarn模式，需要将spark的jars目录下的JAR包都上传到hdfs上

./spark-sql  --master yarn --deploy-mode client 

// 可以执行以下sql进行测试
show tables;
select name,addr,id from linkis_1 group by name,addr,id order by id;
select a.name,a.addr,b.phone from linkis_1 a left join linkis_2 b on a.id=b.id group by a.name,a.addr,b.phone  order by a.name;
```

**ii. Spark 配置文件**

- spark-env.sh

```properties
#!/usr/bin/env bash
SPARK_CONF_DIR=/opt/install/spark/conf
HADOOP_CONF_DIR=/opt/install/hadoop/etc/hadoop
YARN_CONF_DIR=/opt/install/hadoop/etc/hadoop
SPARK_EXECUTOR_CORES=3
SPARK_EXECUTOR_MEMORY=4g
SPARK_DRIVER_MEMORY=2g
```

- spark-defaults.conf

```properties
spark.yarn.historyServer.address=host:18080
spark.yarn.historyServer.allowTracking=true
spark.eventLog.dir=hdfs://host/spark/eventlogs
spark.eventLog.enabled=true
spark.history.fs.logDirectory=hdfs://host/spark/hisLogs
spark.yarn.jars=hdfs://host/spark-jars/*
```

**iii. Linkis 测试**

在 Scriptis 面板新建脚本，脚本类型选择 Sql 即可。基于 hive-testbench 的测试，同样提供了 Spark query 语句，可以参考此场景进行测试。

```sql
show
tables;
select name, addr, id
from linkis_1
group by name, addr, id
order by id;
select a.name, a.addr, b.phone
from linkis_1 a
         left join linkis_2 b on a.id = b.id
group by a.name, a.addr, b.phone
order by a.name;
```

同样，也可以选择 Scala 类型，在脚本中初始化了 sqlContext，直接执行 sql 语句即可。

```scala
val sql = "show tables"
val df = sqlContext.sql(sql)
df.show()
```

##### 3.4.6.3 UDF 函数

Linkis 提供了便携的方式，方便用户自己实现自定义函数，并在脚本中使用。目前支持 Hive、Spark 引擎插件自定义函数，经测试 Flink 引擎暂不支持创建函数，当前版本插件仅支持部分语法。

通过 DSS 控制台创建的函数，默认为临时函数，当引擎插件启动的时候，在当前会话有效。

- **i. 使用流程**

```
1. 本地开发udf函数，完成打包。
2. 在dss的Scriptis界面上传JAR包。
3. 在dss界面创建函数，指定JAR包、函数名、函数的格式（补充主类）。
4. 选择是否加载。默认为加载，在引擎初始化的时候，会创建临时函数。新增、修改函数都需要重启引擎才能生效。
```

![1](https://upload-images.jianshu.io/upload_images/12555001-10208a15eb6e8968.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![2](https://upload-images.jianshu.io/upload_images/12555001-2bcc76823fd40082.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- **ii. 加载流程**

```
1. 在EngineConnServer中创建EngineConn，会有创建引擎前后的执行逻辑。
2. 执行afterExecutionExecute方法，由UDFLoadEngineConnHook获取所有需要加载的udf函数，查看udf注册格式，进行遍历注册。
3. 从加载流程来看，udf函数的生命周期就是引擎的生命周期，udf函数修改完成后，都要重启引擎才可以生效。
4. udf函数选择加载，会将JAR包放到引擎的classpath路径下，且在引擎创建的时候进行注册；不加载的话，那么classpath路径下便不会有此JAR包，也不会注册；且默认都是会话级别的函数。
5. 详细的加载流程可以通过UdfInfo关键字进行搜索，再查看具体逻辑。
```

- **iii. API 调用**

如果不通过 DSS 控制台进行函数的创建、修改，可以通过 API 的方式，参考 `UDFApi` 查看支持的 API 列表，以下是使用示例：

```
POST http://gateway_ip:8001/api/rest_j/v1/udf/update

{"isShared":false,"udfInfo":{"id":4,"udfName":"testudf2","description":"7777","path":"file:///tmp/linkis/hadoop/udf/hive/hive_function.jar","shared":false,"useFormat":"testudf2()","load":true,"expire":false,"registerFormat":"create temporary function testudf2 as \" com.troila.hive.udf.MaskFromEnds\"","treeId":9,"udfType":0}}
```

##### 3.4.6.4 Linkis 调试方式

除了在 DSS 控制台进行脚本调试，还可以使用客户端的方式、SDK等方式

###### 3.4.6.4.1 客户端方式

使用示例：

```shell
./linkis-cli -engineType spark-2.4.3 -codeType sql -code "select count(*) from default.ct_test;"  -submitUser hadoop -proxyUser hadoop 
./linkis-cli -engineType hive-2.3.3 -codeType sql -code "select count(*) from default.ct_test;"  -submitUser hadoop -proxyUser hadoop 
./linkis-cli -engineType hive-2.3.3 -codeType sql -code "select * from \${table};" -varMap table=default.ct_test  -submitUser hadoop -proxyUser hadoop
```

###### 3.4.6.4.2 SDK 方式

- 引入依赖

```xml

<dependency>
    <groupId>com.webank.wedatasphere.linkis</groupId>
    <artifactId>linkis-computation-client</artifactId>
    <version>${linkis.version}</version>
    <exclusions>
        <exclusion>
            <artifactId>commons-codec</artifactId>
            <groupId>commons-codec</groupId>
        </exclusion>
        <exclusion>
            <artifactId>slf4j-api</artifactId>
            <groupId>org.slf4j</groupId>
        </exclusion>
        <exclusion>
            <artifactId>commons-beanutils</artifactId>
            <groupId>commons-beanutils</groupId>
        </exclusion>
    </exclusions>
</dependency>
```

- Scala 代码示例

```scala
package com.troila.bench.linkis.spark

import com.webank.wedatasphere.linkis.common.utils.Utils
import com.webank.wedatasphere.linkis.httpclient.dws.authentication.StaticAuthenticationStrategy
import com.webank.wedatasphere.linkis.httpclient.dws.config.DWSClientConfigBuilder
import com.webank.wedatasphere.linkis.manager.label.constant.LabelKeyConstant
import com.webank.wedatasphere.linkis.ujes.client.UJESClient
import com.webank.wedatasphere.linkis.ujes.client.request.{JobSubmitAction, ResultSetAction}
import org.apache.commons.io.IOUtils
import java.util
import java.util.concurrent.TimeUnit

object ScalaClientTest {

  def main(args: Array[String]): Unit = {
    val user = "hadoop"
    val username = "hadoop"
    val password = "hadoop"
    val yarnQueue = "default"
    val executeCode = "select name,addr,id from linkis_1 group by name,addr,id order by id"
    val gatewayUrl = "http://gateway_ip:8001"

    // 1. 配置DWSClientBuilder，通过DWSClientBuilder获取一个DWSClientConfig
    val clientConfig = DWSClientConfigBuilder.newBuilder()
      .addServerUrl(gatewayUrl) //指定ServerUrl，Linkis服务器端网关的地址,如http://{ip}:{port}
      .connectionTimeout(30000) //connectionTimeOut 客户端连接超时时间
      .discoveryEnabled(false).discoveryFrequency(1, TimeUnit.MINUTES) //是否启用注册发现，如果启用，会自动发现新启动的Gateway
      .loadbalancerEnabled(true) // 是否启用负载均衡，如果不启用注册发现，则负载均衡没有意义
      .maxConnectionSize(5) //指定最大连接数，即最大并发数
      .retryEnabled(false).readTimeout(30000) //执行失败，是否允许重试
      .setAuthenticationStrategy(new StaticAuthenticationStrategy()) //AuthenticationStrategy Linkis认证方式
      .setAuthTokenKey(username).setAuthTokenValue(password) //认证key，一般为用户名;  认证value，一般为用户名对应的密码
      .setDWSVersion("v1").build() //Linkis后台协议的版本，当前版本为v1

    // 2. 通过DWSClientConfig获取一个UJESClient
    val client = UJESClient(clientConfig)

    try {
      // 3. 开始执行代码
      println("user : " + user + ", code : [" + executeCode + "]")
      val startupMap = new java.util.HashMap[String, Any]()
      startupMap.put("wds.linkis.yarnqueue", yarnQueue) //启动参数配置
      //指定Label
      val labels: util.Map[String, Any] = new util.HashMap[String, Any]
      //添加本次执行所依赖的的标签，如engineLabel
      labels.put(LabelKeyConstant.ENGINE_TYPE_KEY, "spark-2.4.3")
      labels.put(LabelKeyConstant.USER_CREATOR_TYPE_KEY, "hadoop-IDE")
      labels.put(LabelKeyConstant.CODE_TYPE_KEY, "sql")
      //指定source
      val source: util.Map[String, Any] = new util.HashMap[String, Any]
      // 参数替换
      val varMap: util.Map[String, Any] = new util.HashMap[String, Any]
      //      varMap.put("table", "linkis_1")

      val jobExecuteResult = client.submit(JobSubmitAction.builder
        .addExecuteCode(executeCode)
        .setStartupParams(startupMap)
        .setUser(user) //Job提交用户
        .addExecuteUser(user) //实际执行用户
        .setLabels(labels)
        .setSource(source)
        .setVariableMap(varMap)
        .build) //User，请求用户；用于做用户级多租户隔离
      println("execId: " + jobExecuteResult.getExecID + ", taskId: " + jobExecuteResult.taskID)

      // 4. 获取脚本的执行状态
      var jobInfoResult = client.getJobInfo(jobExecuteResult)
      val sleepTimeMills: Int = 1000
      while (!jobInfoResult.isCompleted) {
        // 5. 获取脚本的执行进度
        val progress = client.progress(jobExecuteResult)
        val progressInfo = if (progress.getProgressInfo != null) progress.getProgressInfo.toList else List.empty
        println("progress: " + progress.getProgress + ", progressInfo: " + progressInfo)
        Utils.sleepQuietly(sleepTimeMills)
        jobInfoResult = client.getJobInfo(jobExecuteResult)
      }
      if (!jobInfoResult.isSucceed) {
        println("Failed to execute job: " + jobInfoResult.getMessage)
        throw new Exception(jobInfoResult.getMessage)
      }
      // 6. 获取脚本的Job信息
      val jobInfo = client.getJobInfo(jobExecuteResult)
      // 7. 获取结果集列表（如果用户一次提交多个SQL，会产生多个结果集）
      val resultSetList = jobInfoResult.getResultSetList(client)
      println("All result set list:")
      resultSetList.foreach(println)
      val oneResultSet = jobInfo.getResultSetList(client).head
      // 8. 通过一个结果集信息，获取具体的结果集
      val fileContents = client.resultSet(ResultSetAction.builder().setPath(oneResultSet).setUser(jobExecuteResult.getUser).build()).getFileContent
      println("First fileContents: ")
      println(fileContents)
    } catch {
      case e: Exception => {
        e.printStackTrace()
      }
    }
    IOUtils.closeQuietly(client)
  }
}
```

### 3.5 扩展功能

此部分主要是对 Hive on TEZ 的实践，也包括了对 llap 的支持；另外，自行编译了 Flink 引擎插件，对 Kafka、Elasticsearch、Mysql、CDC 等 Connector 进行了实践，实现了
Redis、MongoDB 的 Sink Connector。

#### 3.5.1 Hive 支持 TEZ 引擎

对于 TEZ 引擎的支持，主要需要修改两个地方：一是 Hive 集群环境需要支持 TEZ；二是 Linkis 引擎插件也需要相应的依赖。切换 TEZ 引擎，若是报错，多是 JAR 包缺少导致或是 guava 包冲突等。测试过程中完成的
JAR 包会上传到网盘留存。

需用户自行下载、编译 TEZ，并完成本地的配置，在本地启动 Hive 客户端，确保是以 TEZ 引擎启动，并成功执行 SQL 逻辑，此过程不再本文赘述。

##### 3.5.1.1 Linkis 操作

为了支持 TEZ 引擎，需要将 `tez-*` 开头的 JAR 包拷贝到 Linkis 的引擎依赖路径下，然后重启 ECM 服务。

对于前期的测试，可能需要经常调整 JAR 包，频繁的启动 ECM 服务，整个过程会比较慢，在测试阶段可以将 JAR 包直接复制到 `engineConnPublickDir` 目录下。ECM 启动之后，会将引擎的 lib 依赖以及 conf
都放到这个公共目录下，之后引擎启动都会从此目录建议软链接。 故可以直接拷贝需要的 JAR 包到此目录下，就不必重启 ECM 服务了。在测试成功后，切记将 JAR
包放到 `linkis/lib/linkis-engineconn-plugins/hive/dist/v2.3.7/lib` 目录下，以免重启服务，导致 JAR 包缺失。

需要拷贝的 JAR 包列表：

```
// linkis/lib/linkis-engineconn-plugins/hive/dist/v2.3.7/lib
// 此目录下，在引擎第一次启动的时候，会生成一个lib.zip的缓存包，若修改了lib下的JAR包，而此压缩包没有更新的话，那么还是无法使用最新的JAR包
tez-api-0.9.2.jar
tez-build-tools-0.9.2.jar
tez-common-0.9.2.jar
tez-dag-0.9.2.jar
tez-examples-0.9.2.jar
tez-ext-service-tests-0.9.2.jar
tez-history-parser-0.9.2.jar
tez-javadoc-tools-0.9.2.jar
tez-job-analyzer-0.9.2.jar
tez-mapreduce-0.9.2.jar
tez-protobuf-history-plugin-0.9.2.jar
tez-runtime-internals-0.9.2.jar
tez-runtime-library-0.9.2.jar
tez-tests-0.9.2.jar
tez-yarn-timeline-history-0.9.2.jar
tez-yarn-timeline-history-with-acls-0.9.2.jar
hadoop-yarn-registry-2.8.5.jar
```

##### 3.5.1.2 本地集群配置

Hive on TEZ 模式下，Hive 的执行模式有两种，一种是 container 模式；另一种是 llap 模式，llap 提供了一种混合模型，它包含一个长驻进程，用于直接与 DataNode 进行 IO 交互， 并紧密地集成在
DAG 的框架中，可以显著提高 hive query 的效率。

###### 3.5.1.2.1 container 模式

- 准备 TEZ 依赖包，上传到 HDFS 上，并完成授权。

```shell
# tez官方文档指出此路径可以是压缩包，也可以是解压之后的JAR文件。经测试，建议直接上传解压后的JAR文件。
hdfs dfs -mkidr /tez_linkis
# tez目录下为编译完tez的完整JAR包
hdfs dfs -put tez  /tez_linkis
# 完成授权，确保linkis提交用户可以读取tez文件
hadoop fs -chmod -R 755 /tez_linkis
```

- 修改 `hive-site.xml`，切换引擎，且配置 container 模式

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
    <property>
        <name>hive.metastore.schema.verification</name>
        <value>false</value>
    </property>
    <property>
        <name>hive.metastore.uris</name>
        <value>thrift://host:9083</value>
    </property>
    <property>
        <name>spark.master</name>
        <value>yarn-cluster</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionURL</name>
        <value>jdbc:mysql://host:3306/hive</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionDriverName</name>
        <value>com.mysql.cj.jdbc.Driver</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionUserName</name>
        <value>root</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionPassword</name>
        <value>MySQL5.7</value>
    </property>
    <property>
        <name>hive.execution.engine</name>
        <value>tez</value>
        <description>修改hive的执行引擎为tez</description>
    </property>

    <!-- container -->
    <property>
        <name>hive.execution.mode</name>
        <value>container</value>
    </property>
</configuration>
```

- 修改 `${hadoop_conf_dir}/etc/hadoop/tez-site.xml`，配置 TEZ 依赖

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
    <property>
        <name>tez.lib.uris</name>
        <value>${fs.defaultFS}/tez_linkis/tez</value>
    </property>
    <!-- tez.lib.uris.classpath配置主要为设置自定义的udf等一些扩展的依赖包位置，可以不指定 -->
    <property>
        <name>tez.lib.uris.classpath</name>
        <value>${fs.defaultFS}/tez_linkis/tez</value>
    </property>
    <property>
        <name>tez.use.cluster.hadoop-libs</name>
        <value>true</value>
    </property>
    <property>
        <name>tez.history.logging.service.class</name>
        <value>org.apache.tez.dag.history.logging.ats.ATSHistoryLoggingService</value>
    </property>
</configuration>
```

###### 3.5.1.2.2 llap 模式

llap 模式下，需要部署 llap 服务，且启动 llap 服务的用户与 Linkis 提交 Hive 作业的用户必须是同一用户，否则会报错 `No LLAP Daemons are running`。

- 参考 container 模式，完成 TEZ 的依赖上传与配置操作

- 修改 `hive-site.xml`，切换引擎，且配置 llap 模式

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
<configuration>
    <property>
        <name>hive.metastore.schema.verification</name>
        <value>false</value>
    </property>
    <property>
        <name>hive.metastore.uris</name>
        <value>thrift://host:9083</value>
    </property>
    <property>
        <name>spark.master</name>
        <value>yarn-cluster</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionURL</name>
        <value>jdbc:mysql://host:3306/hive</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionDriverName</name>
        <value>com.mysql.cj.jdbc.Driver</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionUserName</name>
        <value>root</value>
    </property>
    <property>
        <name>javax.jdo.option.ConnectionPassword</name>
        <value>MySQL5.7</value>
    </property>

    <property>
        <name>hive.execution.engine</name>
        <value>tez</value>
        <description>修改hive的执行引擎为tez</description>
    </property>

    <!-- llap -->
    <property>
        <name>hive.execution.mode</name>
        <value>llap</value>
    </property>
    <property>
        <name>hive.llap.execution.mode</name>
        <value>all</value>
    </property>
    <property>
        <name>hive.llap.daemon.service.hosts</name>
        <value>@llap_service</value>
    </property>
    <property>
        <name>hive.zookeeper.quorum</name>
        <value>ct4:2181,ct5:2181,ct6:2181</value>
    </property>
    <property>
        <name>hive.zookeeper.client.port</name>
        <value>2181</value>
    </property>
    <property>
        <name>hive.llap.daemon.num.executors</name>
        <value>1</value>
    </property>
</configuration>
```

- 部署 llap 服务

如果使用的 hadoop yarn 版本是 3.1.0 以下(不包含 3.1.0)，需要使用 Apache slider 来部署，因为在 hadoop yarn 3.1.0 之前，yarn 本身不支持长时间运行的服务(long
running services)，而 slider 组件是可以打包、管理和部署长时间运行的服务到 yarn 上运行的。

如果使用的 hadoop yarn 版本是 3.1.0 及以上，完全不需要 slider 组件了，因为从 hadoop yarn 3.1.0 开始，yarn 已经合并支持 long running services 了，slider
项目也停止更新了。

我们的 hadoop 版本为 2.8.5，故需要借助 Apache slider 来部署 llap 服务，具体流程如下：

```
1. 安装slider，配置环境变量SLIDER_HOME、PATH等。
2. 执行hive命令，生成llap的启动包，需要保证此处的服务名和hist-site中配置的名字一致。
hive --service llap --name llap_service  --instances 2 --cache 512m --executors 2 --iothreads 2 --size 1024m --xmx 512m --loglevel INFO --javaHome /opt/jdk1.8
3. 由于linkis使用hadoop用户提交任务，为了保证tez的应用可以获取到llap的进程，需要切换到hadoop用户去启动llap服务。如果linkis使用别的用户提交作业，llap也要用相同的用户启动，linkis可以指定，dss控制台默认使用的是hadoop用户。
su hadoop；./llap-slider-31Aug2021/run.sh
4. 验证服务可用，yarn的页面上成功提交llap_service的应用，且User为hadoop，再在服务器上使用 jps 命令查看进程，出现LlapDaemon即表明成功。
5. 此服务只要提交用户相同就可用被其它应用获取，所以只需要在hive的一个节点上启动此服务即可，其它hive节点不需要安装slider、llap-slider启动包等。
```

##### 3.5.1.3 Linkis 脚本测试

本地集群配置完成，且在本地测试成功之后，可以在 DSS 控制台上测试，需要保证 DSS 的登录用户和启动 llap 服务的用户为同一个用户，不然可能会出现 `No LLAP Daemons are running` 的报错，也可以使用
API 方式，切换执行用户：

```
// userCreator可以指定为hadoop-IDE，那么user就是hadoop。
POST http://gateway_ip:8001/api/rest_j/v1/entrance/submit

{
    "executionContent": {"code": "select name,addr,id from linkis_1 group by name,addr,id order by id", "runType":  "sql"},
    "params": {"variable": {}, "configuration": {}},
    "source":  {"scriptPath": ""},
    "labels": {
        "engineType": "hive-2.3.7",
        "userCreator": "root-IDE"
    }
}
```

#### 3.5.2 Flink 引擎支持

Linkis 1.0.2 中已经集成了 Flink 引擎，但是在编译时，不会放到安装包中，需要以新增引擎的方式，手动配置。

对于 Flink 引擎插件的调试，大多是 JAR 包问题导致。需要保证 `${flink_lib_dir}` 和 Linkis 的 Flink 引擎目录下都存在所需 Connector 包和 format 包。 目前，调试通过
Kafka、Mysql、CDC、Elasticsearch、Redis、MongoDB 等 Connector，数据格式支持 CSV、JSON 等。会将完整 JAR 包放到网盘上留存。

一般来讲，Flink Conector 的调试大部分为找不到类的错误。可以从以下思路来解决：

- 如果是`Could not find any factory for identifier 'elasticsearch-7' that implements 'org.apache.flink.table.factories.DynamicTableFactory' in the classpath.`
这种错误，一般是 Linkis 引擎插件目录下没有相应的 Connector 包，因为引擎插件目录下的包，会在启动的时候放到 classpath 上。

- 如果是`Caused by: java.lang.ClassNotFoundException: org.apache.flink.connector.jdbc.table.JdbcRowDataInputFormat`这种错误，明明
  classpath 上已经存在这个包，且包中含有此类，一般是由于 Flink 的 lin 目录下没有这个包。

- 另外对于一些有 sql-connector 的连接器包，优先使用此包，这个包会引入 Connector 包，所以直接用 sql-connector 包即可。

- 对于某些特殊数据格式的，需要自行编译 Flink format 放到 lib 目录和 Linkis 引擎目录下，目前支持 CSV、JSON 格式，对于 Debezium、Maxwell、Canal 等需要自行编译。

##### 3.5.2.1 本地安装 Flink

**i. 下载安装包**

可以直接下载官网提供的编译好的安装包，也可以自己下载源码自行编译，对应 Scala 版本选择为 2.11，避免因 Scala 版本不一致出现问题。

**ii. Flink 配置文件**

- flink-conf.yaml

`vim flink-conf.yaml` 配置 JDK 等信息，配置示例：

```yaml
jobmanager.archive.fs.dir: hdfs://ct4:8020/flink-test
env.java.home: /opt/jdk1.8
classloader.resolve-order: parent-first
parallelism.default: 1
taskmanager.numberOfTaskSlots: 1
historyserver.archive.fs.dir: hdfs://ct4:8020/flink
jobmanager.rpc.port: 6123
taskmanager.heap.size: 1024m
jobmanager.heap.size: 1024m
rest.address: ct6
```

- 配置环境变量

在环境检查中已经给出了环境变量的示例，参考示例即可。

**iii. 选择性编译**

Flink 提供了多种 format，以支持不同数据格式转换，默认安装包中提供了 CSV、JSON等转换，对于Avro、Orc、Raw、Parquet、Maxwell、Canal、Debezium等需要自行编译。

Flink 提供了多种 Connector，以支持不同数据源的 Source、Sink等，默认安装包并不会全部提供，需要自行编译。

- 编译流程：

```
1. 先格式化代码 
mvn spotless:apply
2. 打包编译 
mvn clean install -Dmaven.test.skip=true
```

##### 3.5.2.2 新增 Flink 引擎插件

因为 Linkis1.0.2 并不会将 Flink
引擎自动写入到引擎插件中，需要用户手动新增引擎插件，详细可以参考 **[引擎插件安装文档](https://github.com/WeBankFinTech/Linkis-Doc/blob/master/zh_CN/Deployment_Documents/EngineConnPlugin%E5%BC%95%E6%93%8E%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85%E6%96%87%E6%A1%A3.md)**

Linkis1.0.2版本跟官方文档描述略有差异，以下是计算层安装流程：

```
1. 在linkis项目中手动编译flink插件，编译完成之后拷贝并上传flink-engineconn.zip
mvn clean install -Dmaven.test.skip=true

2. 解压压缩文件 flink-engineconn.zip 到 `${LINKIS_HOME}/lib/linkis-engineconn-plugins` 目录下
unzip flink-engineconn.zip

3. 上传所需的connector包和数据格式转换包，共有两个目录需要上传，以下是目录示例：
${LINKIS_HOME}/lib/linkis-engineconn-plugins/flink/dist/v1.12.2/lib
${FLINK_HOME}/lib

4. 刷新引擎。通过restful接口热加载引擎，请求 `LINKIS-CG-ENGINEPLUGIN` 服务，可以在配置文件中获取此服务的端口号。
POST http://LINKIS-CG-ENGINEPLUGIN_IP:LINKIS-CG-ENGINEPLUGIN_PORT/api/rest_j/v1/rpc/receiveAndReply
{
  "method": "/enginePlugin/engineConn/refreshAll"
}

5. 可选操作，新增引擎的参数需要动态管理，可以添加引擎参数到linkis的元数据库中，这样在 管理台-->参数配置 可以可视化的修改引擎启动的参数。可以参考初始化的sql语句和flink插件的配置进行插入操作。

```

- 基本测试

通过 DSS 控制台，提交基础的测试脚本，保证可以正常执行：

```sql
SELECT 'linkis flink engine test!!!';
SELECT name, COUNT(*) AS cnt
FROM (VALUES ('Bob'), ('Alice'), ('Greg'), ('Bob')) AS NameTable(name)
GROUP BY name;
```

##### 3.5.2.3 Flink Connector 调试

Flink Connector 的调试大部分是 JAR 包的问题，完整 JAR 包已经放到网盘上。

```
链接：https://pan.baidu.com/s/17g05rtfE_JSt93Du9TXVug 
提取码：zpep
```

再强调一点，保证 Connector 包和 format 包，在 Linkis 的引擎目录以及 Flink 的安装目录都上传一份。

###### 3.5.2.3.1 Kafka Connector

Kafka Connector 即可以作为 Source，也可以作为 Sink。

- 根据上文的编译方法，编译 `flink-sql-connector-kafka_2.11-1.12.2.jar` 包，并上传到上文提到的两个目录

- 测试脚本

```sql
CREATE TABLE source_kafka
(
    id   STRING,
    name STRING,
    age  INT
) WITH (
      'connector' = 'kafka',
      'topic' = 'flink_sql_1',
      'scan.startup.mode' = 'earliest-offset',
      'properties.bootstrap.servers' = 'ct4:9092,ct5:9092,ct6:9092',
      'format' = 'json'
      );
CREATE TABLE sink_kafka
(
    id   STRING,
    name STRING,
    age  INT,
    PRIMARY KEY (id) NOT ENFORCED
) WITH (
      'connector' = 'upsert-kafka',
      'topic' = 'flink_sql_3',
      'properties.bootstrap.servers' = 'ct4:9092,ct5:9092,ct6:9092',
      'key.format' = 'json',
      'value.format' = 'json'
      );
INSERT INTO sink_kafka
SELECT `id`,
       `name`,
       `age`
FROM source_kafka;
```

详细配置参考 [Apache Kafka SQL Connector](https://ci.apache.org/projects/flink/flink-docs-release-1.12/zh/dev/table/connectors/kafka.html)

###### 3.5.2.3.2 Mysql Connector

Mysql Connector 即可以作为 Source，也可以作为 Sink，作为 Source 不会实时监听数据库的变化。

- 上传 `flink-connector-jdbc_2.11-1.12.2.jar` 和 `mysql-connector-java-5.1.49.jar` 到以上两个目录

- 测试脚本

```sql
CREATE TABLE source_mysql
(
    id   STRING,
    name STRING,
    age  int,
    PRIMARY KEY (id) NOT ENFORCED
) WITH (
      'connector' = 'jdbc',
      'url' = 'jdbc:mysql://host:3306/computation',
      'table-name' = 'flink_sql_1',
      'username' = 'root',
      'password' = 'MySQL5.7'
      );
CREATE TABLE sink_kafka
(
    id   STRING,
    name STRING,
    age  INT,
    PRIMARY KEY (id) NOT ENFORCED
) WITH (
      'connector' = 'upsert-kafka',
      'topic' = 'flink_sql_3',
      'properties.bootstrap.servers' = 'ct4:9092,ct5:9092,ct6:9092',
      'key.format' = 'json',
      'value.format' = 'json'
      );
INSERT INTO sink_kafka
SELECT `id`,
       `name`,
       `age`
FROM source_mysql;
```

详细配置参考 [JDBC SQL Connector](https://ci.apache.org/projects/flink/flink-docs-release-1.12/zh/dev/table/connectors/jdbc.html)

###### 3.5.2.3.3 Mysql CDC Connector

Mysql CDC Connector 可以作为 Source，实时监听数据库的变化，并发送到 Flink SQL Source 中，从而省去了使用 Debezium、Canal 或 Maxwell 等工具的二次发送。

[flink-connector-mysql-cdc](https://mvnrepository.com/artifact/com.alibaba.ververica/flink-connector-mysql-cdc/1.2.0)
可以直接点击下载，此包由 [Ververica](https://developer.aliyun.com/article/724113) 提供，兼容了 Flink 1.12，可以直接使用。

- 上传 `flink-connector-mysql-cdc-1.2.0.jar` 和 `mysql-connector-java-5.1.49.jar` 到以上两个目录

- 测试脚本

```sql
CREATE TABLE mysql_binlog
(
    id   STRING NOT NULL,
    name STRING,
    age  INT
) WITH (
      'connector' = 'mysql-cdc',
      'hostname' = 'host',
      'port' = '3306',
      'username' = 'root',
      'password' = 'MySQL5.7',
      'database-name' = 'flink_sql_db',
      'table-name' = 'flink_sql_2',
      'debezium.snapshot.locking.mode' = 'none' --建议添加,不然会要求锁表
      );
CREATE TABLE sink_kafka
(
    id   STRING,
    name STRING,
    age  INT,
    PRIMARY KEY (id) NOT ENFORCED
) WITH (
      'connector' = 'upsert-kafka',
      'topic' = 'flink_sql_3',
      'properties.bootstrap.servers' = 'ct4:9092,ct5:9092,ct6:9092',
      'key.format' = 'json',
      'value.format' = 'json'
      );
INSERT INTO sink_kafka
SELECT `id`,
       `name`,
       `age`
FROM mysql_binlog;
```

###### 3.5.2.3.4 Elasticsearch Connector

Elasticsearch Connector 可以作为 Sink 端，将数据持久化到 ES 中，选择对应的版本，进行编译，如果是 Flink
SQL，建议直接编译 `flink-sql-connector-elasticsearch7_2.11` 即可。

- 上传 `flink-sql-connector-elasticsearch7_2.11-1.12.2.jar` 到以上两个目录

- 测试脚本

```sql
CREATE TABLE mysql_binlog
(
    id   STRING NOT NULL,
    name STRING,
    age  INT
) WITH (
      'connector' = 'mysql-cdc',
      'hostname' = 'host',
      'port' = '3306',
      'username' = 'root',
      'password' = 'MySQL5.7',
      'database-name' = 'flink_sql_db',
      'table-name' = 'flink_sql_2',
      'debezium.snapshot.locking.mode' = 'none' --建议添加,不然会要求锁表
      );
CREATE TABLE sink_es
(
    id   STRING,
    name STRING,
    age  INT,
    PRIMARY KEY (id) NOT ENFORCED
) WITH (
      'connector' = 'elasticsearch-7',
      'hosts' = 'http://host:9200',
      'index' = 'flink_sql_cdc'
      );
INSERT INTO sink_es
SELECT `id`,
       `name`,
       `age`
FROM mysql_binlog;
```

详细配置参考 [Elasticsearch SQL Connector](https://ci.apache.org/projects/flink/flink-docs-release-1.12/zh/dev/table/connectors/elasticsearch.html)

##### 3.5.2.4 自定义开发 Connector

Flink 官方提供的 Connector 有限，对于某些需要将数据通过 Flink SQL 推送到 Redis、MongoDB 的场景就不能很好的满足，因此需要开发对应的 Connector 来处理数据推送。 目前开发的
Redis、MongoDB Connector 只支持 Sink 操作。

完整的代码的已经上传的 github，可以参考  **[flink-connector](https://github.com/mindflow94/flink-connector)**

另外，**[bahir-flink](https://github.com/apache/bahir-flink)** 上也维护了很多 Flink 官方没有的 Connector，有需要可以参考。

###### 3.5.2.4.1 Redis Connector

Redis Connector 的开发是依据 **[bahir-flink](https://github.com/apache/bahir-flink)** 中的 Redis 连接器，支持哨兵模式、集群模式的配置。主要做了两方面的优化：

```
1. 新增单机版 Redis 的连接配置与处理逻辑
2. 删除了代码中启用的代码，使用新版本的 `DynamicTableSink`、`DynamicTableSinkFactory` 来实现动态 Sink 处理
```

- 上传 `flink-connector-redis_2.11.jar` 到以上两个目录

- 测试脚本

```sql
CREATE TABLE datagen
(
    id   INT,
    name STRING
) WITH (
      'connector' = 'datagen',
      'rows-per-second' = '1',
      'fields.name.length' = '10'
      );
CREATE TABLE redis
(
    name STRING,
    id   INT
) WITH (
      'connector' = 'redis',
      'redis.mode' = 'single',
      'command' = 'SETEX',
      'single.host' = '172.0.0.1',
      'single.port' = '6379',
      'single.db' = '0',
      'key.ttl' = '60',
      'single.password' = 'password'
      );
insert into redis
select name, id
from datagen;
```

详细说明参考 [flink-connector-redis 说明](https://github.com/mindflow94/flink-connector/blob/master/flink-connector-redis/README.md)

###### 3.5.2.4.2 MongoDB Connector

MongoDB Connector 的开发参考 **[Ververica-Connector](https://mvnrepository.com/search?q=Ververica)** 的 MongoDB 连接器，保留了核心处理逻辑。

开发流程可以参考文章 [Flink SQL Connector MongoDB 开发指南](https://blog.csdn.net/zyz_Alvin/article/details/120351635)

- 上传 `flink-connector-mongodb_2.11.jar` 到以上两个目录

- 测试脚本

```sql
CREATE TABLE datagen
(
    id   INT,
    name STRING
) WITH (
      'connector' = 'datagen',
      'rows-per-second' = '1',
      'fields.name.length' = '10'
      );
CREATE TABLE mongoddb
(
    id   INT,
    name STRING
) WITH (
      'connector' = 'mongodb',
      'database' = 'mongoDBTest',
      'collection' = 'flink_test',
      'uri' = 'mongodb://user:passeord@172.0.0.1:27017/?authSource=mongoDBTest',
      'maxConnectionIdleTime' = '20000',
      'batchSize' = '1'
      );
insert into mongoddb
select id, name
from datagen;
```

##### 3.5.2.5 提交 Flink 作业

通过 DSS 的 Scriptis 提交 Flink SQL 作业，启动的是 session 模式，适用于 select 语法，查看数据或测试，对于 insert 语法，默认 3 min，会杀掉任务。因此， 这种 Scriptis
的方式，并不适合 long running 的任务。生产环境中，对于这种任务，应该采用 onceJob 的方式提交，即 Flink 中 pre-job 的方式。

- 引入 `linkis-computation-client` pom 依赖

```xml

<dependency>
    <groupId>com.webank.wedatasphere.linkis</groupId>
    <artifactId>linkis-computation-client</artifactId>
    <version>${linkis.version}</version>
    <exclusions>
        <exclusion>
            <artifactId>commons-codec</artifactId>
            <groupId>commons-codec</groupId>
        </exclusion>
        <exclusion>
            <artifactId>slf4j-api</artifactId>
            <groupId>org.slf4j</groupId>
        </exclusion>
        <exclusion>
            <artifactId>commons-beanutils</artifactId>
            <groupId>commons-beanutils</groupId>
        </exclusion>
    </exclusions>
</dependency>
```

- `resources` 下配置 `linkis.properties` 指定 gateway 地址

```properties
wds.linkis.server.version=v1
wds.linkis.gateway.url=http://host:8001/
```

- 代码示例

```scala
import com.webank.wedatasphere.linkis.common.conf.Configuration
import com.webank.wedatasphere.linkis.computation.client.once.simple.SimpleOnceJob
import com.webank.wedatasphere.linkis.computation.client.utils.LabelKeyUtils
import com.webank.wedatasphere.linkis.manager.label.constant.LabelKeyConstant

/**
 * Created on 2021/8/24.
 *
 * @author MariaCarrie
 */
object OnceJobTest {

  def main(args: Array[String]): Unit = {
    val sql =
      """CREATE TABLE source_from_kafka_8 (
        |  id STRING,
        |  name STRING,
        |  age INT
        |) WITH (
        |    'connector' = 'kafka',
        |    'topic' = 'flink_sql_1',
        |    'scan.startup.mode' = 'earliest-offset',
        |    'properties.bootstrap.servers' = 'ct4:9092,ct5:9092,ct6:9092',
        |    'format' = 'json'
        |);
        |CREATE TABLE sink_es_table1 (
        |  id STRING,
        |  name STRING,
        |  age INT,
        |  PRIMARY KEY (id) NOT ENFORCED
        |) WITH (
        |  'connector' = 'elasticsearch-7',
        |  'hosts' = 'http://host:9200',
        |  'index' = 'flink_sql_8'
        |);
        |INSERT INTO
        |  sink_es_table1
        |SELECT
        |  `id`,
        |  `name`,
        |  `age`
        |FROM
        |  source_from_kafka_8;
        |""".stripMargin

    val onceJob = SimpleOnceJob.builder().setCreateService("Flink-Test").addLabel(LabelKeyUtils.ENGINE_TYPE_LABEL_KEY, "flink-1.12.2")
      .addLabel(LabelKeyUtils.USER_CREATOR_LABEL_KEY, "hadoop-Streamis").addLabel(LabelKeyUtils.ENGINE_CONN_MODE_LABEL_KEY, "once")
      .addStartupParam(Configuration.IS_TEST_MODE.key, true)
      .addStartupParam("flink.taskmanager.numberOfTaskSlots", 4)
      .addStartupParam("flink.container.num", 4)
      .addStartupParam("wds.linkis.engineconn.flink.app.parallelism", 8)
      .addStartupParam(Configuration.IS_TEST_MODE.key, true)
      .setMaxSubmitTime(300000)
      .addExecuteUser("hadoop").addJobContent("runType", "sql").addJobContent("code", sql).addSource("jobName", "OnceJobTest")
      .build()

    onceJob.submit()
    onceJob.waitForCompleted()
    System.exit(0)
  }
}

```

## 4. 最佳实践

### 4.1 Hive

#### 4.1.1 权限不足导致引擎启动失败

- **问题描述**

通过 Linkis 提交作业，引擎启动失败。

- **详细报错**

```log
Error: Could not find or load main class com.webank.wedatasphere.linkis.engineconn.launch.EngineConnServer

Caused by: LinkisException{errCode=10010, desc='DataWorkCloud service must set the version, please add property [[wds.linkis.server.version]] to properties file.', ip='null', port=0, serviceKind='null'}
```

- **解决方案**

以上两个报错都是引擎权限不足导致，无法加载 JAR 文件或配置文件。第一次启动引擎，Linkis 会将各类引擎的依赖，放到 `engineConnPublickDir` 下，包括 lib 和 conf。 在创建引擎的时候会创建 engine
目录，生成 `engineConnExec.sh`，并和 `engineConnPublickDir` 下的 lib、conf 建立软链接。导致这个问题出现的原因就是`engineConnPublickDir`下权限不足。

优化`handleInitEngineConnResources`方法，在初始化引擎的时候，完成授权操作。重新编译`linkis-engineconn-manager-server`
包，替换`linkis/lib/linkis-computation-governance/linkis-cg-engineconnmanager`目录下的 JAR，然后单独重启 ECM 服务。代码如下：

```scala
// todo fix bug. Failed to load com.webank.wedatasphere.linkis.engineconn.launch.EngineConnServer.
val publicDir = localDirsHandleService.getEngineConnPublicDir
val bmlResourceDir = Paths.get(publicDir).toFile.getPath
val permissions = Array(PosixFilePermission.OWNER_READ, PosixFilePermission.OWNER_WRITE, PosixFilePermission.OWNER_EXECUTE, PosixFilePermission.GROUP_READ, PosixFilePermission.GROUP_WRITE, PosixFilePermission.GROUP_EXECUTE, PosixFilePermission.OTHERS_READ, PosixFilePermission.OTHERS_WRITE, PosixFilePermission.OTHERS_EXECUTE)
// 授权根路径
warn(s"Start changePermission ${ENGINECONN_ROOT_DIR}")
changePermission(ENGINECONN_ROOT_DIR, true, permissions)

private def changePermission(pathStr: String, isRecurisive: Boolean, permissions: Array[PosixFilePermission]): Unit = {
  val path = Paths.get(pathStr)
  if (!Files.exists(path)) {
    warn(s"ChangePermission ${pathStr} not exists!")
    return
  }
  try {
    val perms = new util.HashSet[PosixFilePermission]()
    for (permission <- permissions) {
      perms.add(permission)
    }
    Files.setPosixFilePermissions(path, perms)
    warn(s"Finish setPosixFilePermissions ${pathStr} ")
  } catch {
    case e: IOException =>
      if (e.isInstanceOf[UserPrincipalNotFoundException]) {
        return
      }
      e.printStackTrace()
  }
  // 当是目录的时候，递归设置文件权限
  if (isRecurisive && Files.isDirectory(path)) {
    try {
      val ds = Files.newDirectoryStream(path)
      import java.io.File
      import scala.collection.JavaConversions._
      for (subPath <- ds) {
        warn(s"Recurisive setPosixFilePermissions ${subPath.getFileName} ")
        changePermission(pathStr + File.separator + subPath.getFileName, true, permissions)
      }
    } catch {
      case e: Exception => e.printStackTrace()
    }
  }
}
```

#### 4.1.2 Container exited with a non-zero exit code 1

- **问题描述**
  
切换了 TEZ 引擎，通过 Linkis 提交 Hive 作业，引擎可以成功启动，也作业已已经提交到 YARN 上，不过执行状态一直失败。

- **详细报错**
  
```log
2021-08-30 11:18:33.018 ERROR SubJob : 73 failed to execute task, code : 21304, reason : Task is Failed,errorMsg: errCode: 12003 ,desc: MatchError: LinkisException{errCode=30002, desc='failed to init engine .reason:SessionNotRunning: TezSession has already shutdown. Application application_1630056358308_0012 failed 2 times due to AM Container for appattempt_1630056358308_0012_000002 exited with  exitCode: 1

yarn上application报错信息：`Error: Could not find or load main class org.apache.tez.dag.app.DAGAppMaster`
```

- **解决方案**

启用了 TEZ 引擎，但是引擎依赖的 JAR 包不能完整读取到，TEZ 官网是支持配置压缩文件和解压文件的，但是在与 Linkis 集成时，配置压缩文件会出现此问题。

上传本地已经解压的 TEZ 依赖文件夹，修改 `tez-site.xml` 中 `tez.lib.uris` 为解压后的目录及子目录。

#### 4.1.3 NoSuchMethodError

- **问题描述**
  
切换了 TEZ 引擎，且配置了 `hive.execution.mode` 为 llap。通过 Linkis 提交作业时，引擎可以成功创建，作业也可以提交到 YARN 上，执行失败。

- **详细报错**
  
```log
linkis控制台报错：return code 1 from org.apache.hadoop.hive.ql.exec.tez.TezTask

yarn上application报错：
2021-08-30 16:04:35,564 [FATAL] [org.apache.hadoop.hive.common.JvmPauseMonitor$Monitor@48abb5a6] |yarn.YarnUncaughtExceptionHandler|: Thread Thread[org.apache.hadoop.hive.common.JvmPauseMonitor$Monitor@48abb5a6,5,main] threw an Error.  Shutting down now...
java.lang.NoSuchMethodError: com.google.common.base.Stopwatch.elapsed(Ljava/util/concurrent/TimeUnit;)J
	at org.apache.hadoop.hive.common.JvmPauseMonitor$Monitor.run(JvmPauseMonitor.java:185)
	at java.lang.Thread.run(Thread.java:748)
```

- **解决方案**

由于 TEZ 依赖的 guava 版本过低导致，本地 Hive 执行时，可以从本地加载到高版本的 guava，而上传到 HDFS 上的 TEZ 依赖 guava 版本过低。

拷贝 `hive/lib` 下高版本的 guava 包，上传到 `tez.lib.uris` 目录下。

#### 4.1.4 No LLAP Daemons are running

- **问题描述**

切换了 TEZ 引擎，且配置了 `hive.execution.mode` 为 llap。通过 Linkis 提交作业时，引擎可以成功创建，作业也可以提交到 YARN 上，Linkis 的引擎日志中报错。

- **详细报错**
  
```log
2021-08-31 18:05:11.421 ERROR [BDP-Default-Scheduler-Thread-3] SessionState 1130 printError - Status: Failed
Dag received [DAG_TERMINATE, SERVICE_PLUGIN_ERROR] in RUNNING state.
2021-08-31 18:05:11.421 ERROR [BDP-Default-Scheduler-Thread-3] SessionState 1130 printError - Dag received [DAG_TERMINATE, SERVICE_PLUGIN_ERROR] in RUNNING state.
Error reported by TaskScheduler [[2:LLAP]][SERVICE_UNAVAILABLE] No LLAP Daemons are running
2021-08-31 18:05:11.422 ERROR [BDP-Default-Scheduler-Thread-3] SessionState 1130 printError - Error reported by TaskScheduler [[2:LLAP]][SERVICE_UNAVAILABLE] No LLAP Daemons are running
Vertex killed, vertexName=Reducer 3, vertexId=vertex_1630056358308_0143_1_02, diagnostics=[Vertex received Kill while in RUNNING state., Vertex did not succeed due to DAG_TERMINATED, failedTasks:0 killedTasks:1, Vertex vertex_1630056358308_0143_1_02 [Reducer 3] killed/failed due to:DAG_TERMINATED]
2021-08-31 18:05:11.422 ERROR [BDP-Default-Scheduler-Thread-3] SessionState 1130 printError - Vertex killed, vertexName=Reducer 3, vertexId=vertex_1630056358308_0143_1_02, diagnostics=[Vertex received Kill while in RUNNING state., Vertex did not succeed due to DAG_TERMINATED, failedTasks:0 killedTasks:1, Vertex vertex_1630056358308_0143_1_02 [Reducer 3] killed/failed due to:DAG_TERMINATED]
Vertex killed, vertexName=Reducer 2, vertexId=vertex_1630056358308_0143_1_01, diagnostics=[Vertex received Kill while in RUNNING state., Vertex did not succeed due to DAG_TERMINATED, failedTasks:0 killedTasks:1, Vertex vertex_1630056358308_0143_1_01 [Reducer 2] killed/failed due to:DAG_TERMINATED]
```

- **解决方案**

由于 llap 服务的启动用户与 Linkis 提交任务的用户不同，导致 Linkis 的用户无法获取 llap 进程。

指定 Linkis 的用户，或者使用 Linkis 用户启动 llap 服务。

### 4.2 Spark

#### 4.2.1 ClassNotFoundException

- **问题描述**

本地 Spark 集群安装完毕，使用 Linkis 提交 Spark SQL 作业，Spark 引擎可以成功启动，但是提交 Spark 作业出错

- **详细报错**

```log
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.JavaMainApplication.start(SparkApplication.scala:52)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit.org$apache$spark$deploy$SparkSubmit$$runMain(SparkSubmit.scala:849)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit.doRunMain$1(SparkSubmit.scala:167)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit.submit(SparkSubmit.scala:195)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit.doSubmit(SparkSubmit.scala:86)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit$$anon$2.doSubmit(SparkSubmit.scala:924)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit$.main(SparkSubmit.scala:933)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at org.apache.spark.deploy.SparkSubmit.main(SparkSubmit.scala)
68e048a8-c4b2-4bc2-a049-105064bea6dc:Caused by: java.lang.ClassNotFoundException: scala.Product$class
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at java.net.URLClassLoader.findClass(URLClassLoader.java:382)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:355)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
68e048a8-c4b2-4bc2-a049-105064bea6dc:	... 20 more
```

- **解决方案**

由于本地 Spark 集群采用的是 Scala 2.12 版本编译，而 Spark 引擎插件是使用 Scala 2.11 编译，导致 `scala.Product` 无法找到。

本地集群使用 Scala 2.11 重新编译，一定要注意 Linkis 引擎插件的 Scala、SDK等版本与集群中的版本一致。

#### 4.2.2 ClassCastException

- **问题描述**

本地使用 `spark-sql` 可以成功提交、执行 Spark SQL 作业，使用 Linkis 提交的 Spark SQL 作业无法运行。

- **详细报错**

```log
Caused by: java.lang.ClassCastException: cannot assign instance of scala.collection.immutable.List$SerializationProxy to field org.apache.spark.rdd.RDD.dependencies_ of type scala.collection.Seq in instance of org.apache.spark.rdd.MapPartitionsRDD
```

- **解决方案**

由于 `spark-sql` 未指定 YARN 的 deploy-mode，因此从 `spark/lib` 下拉取依赖。而 `spark-defaults.conf` 中配置的 `spark.yarn.jars` 路径下的 JAR
包，未包含 Hive 的依赖。

上传本地含 Hive 支持的依赖到 `spark.yarn.jars` 路径，执行 `./spark-sql --master yarn --deploy-mode client` ，保证可以成功执行，再使用 Linkis 提交任务。

### 4.3 Flink

#### 4.3.1 method did not exist

- **问题描述**

开发完成 MongoDB Connector ，本地测试没有问题，数据可以成功写入。将 JAR 包上传至 Linkis 引擎插件中，通过 Linkis 提交 Flink 作业报错，导致 Spring Boot 作业无法正常启动。

- **详细报错**

```log
***************************
APPLICATION FAILED TO START
***************************
Description:
An attempt was made to call a method that does not exist. The attempt was made from the following location:
    org.springframework.boot.autoconfigure.mongo.MongoClientFactorySupport.applyUuidRepresentation(MongoClientFactorySupport.java:85)
The following method did not exist:
    com.mongodb.MongoClientSettings$Builder.uuidRepresentation(Lorg/bson/UuidRepresentation;)Lcom/mongodb/MongoClientSettings$Builder;
```

- **解决方案**

由于引入了 MongoDB 连接器，Spring Boot 的 MongoAutoConfiguration 会使用连接器中的 `mongoclient`，由于自定义 MongoDB 连接器版本不一致导致。

对于需要使用 Spring Boot 项目的，需要格外注意 Spring Boot 中内置的 Mongo 版本，此次升级了连接器中 Mongo driver 的版本。

## 5. 参考

**[https://github.com/WeBankFinTech/Linkis-Doc](https://github.com/WeBankFinTech/Linkis-Doc)**

**[https://github.com/WeBankFinTech/DataSphereStudio-Doc](https://github.com/WeBankFinTech/DataSphereStudio-Doc)**

**[https://github.com/apache/tez](https://github.com/apache/tez)**

**[Flink Table & SQL Connectors 官网](https://ci.apache.org/projects/flink/flink-docs-release-1.12/zh/dev/table/connectors/)**

