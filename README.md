**简历**

## 0x0100 个人简介

* 姓名: 许友正
* 出生年月: 1984.12
* 教育背景: 2005-2009山东大学物理专业, 本科
* 手机: 15759268138
* 邮箱: xuyouzhengzhenghe@126.com
* 居住所在地: 厦门
* github主页:  [https://github.com/oylz](https://github.com/oylz)
* 主攻方向: 架构设计、高并发低延时基础组件、apm(应用性能管理)、计算机视觉(人工智能)

技能/语言|c++|java|linux|架构优化|性能调优|人工智能
-|-|-|-|-|-|-
自评分(满分10)|9|7|8.5|8|9|7

## 0x0200 工作经历

### 0x0201 厦门亿联(2018.02-2020.01, Teamleader, 架构设计,基础组件)

   前期主导云服务端架构重构,让亿联云视频真正**云化**;中期专注基础组件建设\(数据中心\[postgresql&redis全球同步\], 接入服务, 推送服务\);后期专注微服务性能管理\(全链路追踪\);

   ```技能项(c++,java,postgresql,redis,rocksdb,rocketmq,gperftools,vargrind,netty)```

### 0x0202 深图智服(2017.03-2018.01, 架构师,计算机视觉)

   主导智能安防系统架构设计,涉足人脸分析\(检测、跟踪、识别\)、视频相关\(编码合流&推流、拉流解码\);

   ```技能项(c++,redis,caffe,tensorflow,ffmpeg, pvanet, mtcnn, vgg, resnet, dlib, flann, opencv)```

### 0x0203 网宿科技(2016.07-2017.03, 架构师, 连麦/直播)

   主导直播交互系统架构设计;

   ```技能项(c++,java,redis,twemproxy,netty,rocketmq,solr)```

### 0x0204 公安三所(2013.03-2016.06, 技术主管, 大数据)

   前期实现百亿级记录秒级检索;中后期从事高速卡口相关\(车牌识别、危化车识别、人车绑定\)及安防相关\(枪球联动一体机\[人脸检测识别、相机标定\]\);

   ```技能项(c++,java,hadoop,hbase,hive,spark,solr,mysql,cobar,caffe,HDFS,GPFS,ClusterFS, svm, caffe, alexnet, vgg, opencv)```

### 0x0205 上海歌联(2012.12-2013.03, c++主程, 智能物流)

   主导智能物流系统架构设计及服务端实现;

   ```技能项(c++,电子栅栏)```

### 0x0206 盘石软件(2009.04-2012.11, 组长, 计算机取证)

   文件系统解析,数据文件破解,数据恢复;

   ```技能项(c++, java, hadoop, hbase)```

## 0x0300 主要项目经历

### 0x0301 应用性能管理
* 旁路抓包, 网络报文解析,面向协议(postgresql,thrift,rocketmq,http,redis)
* c/c++运行时注入
* java字节码注入(bytebuddy)
* postgresql审计
* skywalking存储对接(elasticsearch,protobuf)

### 0x0302 数据同步组件
* 全球同步, 最终一致, 异地多活
* 回环控制:postgresql二次开发\(语法层、持久化层扩展\[sync_insert,sync_update,sync_delete\]\)， redis二次开发\(插件命令扩展\[sync_\*\]\)
* 多写控制: 优先级向量时钟设计实现
* redis组件添加\(hash field过期实现, AOF&RDB文件解析及同步\) 
* redis智能客户端
* 性能瓶颈分析及优化\(gperftools,vargrind\)

### 0x0303 IM/推送服务
* 接入层设计
* 读扩散写扩散结合, 历史库实时库分离
* 消息同步协议设计

### 0x0304 智能安防
* 人脸检测(pvanet,mtcnn,dlib)、识别(vgg,resnet)
* [多目标跟踪, 已对外开源 https://github.com/oylz/DS](https://github.com/oylz/DS)
* [caffe添加face_proposal层,已对外开源 https://github.com/oylz/caffe-pvanet-shufflenet](https://github.com/oylz/caffe-pvanet-shufflenet)
* 视频编解码(ffmpeg)

### 0x0305 连麦
* 异地双活(redis,rocketmq)
* 50万并发, 实时推送(netty)
* 性能调优(jvmvisual)

### 0x0306 公安大数据系统
* 高性能并行计算集群

主要负责搭建一个集群管理和资源调度的系统。当前主要并行计算平台都有自己的一套任务调度算法，而工程越来越细化和复杂化，只使用一个并行计算平台已经无法满足要求。为此，根据每个模块的特性和要求，选择适合的并行计算平台。由此带来的各平台的不兼容性，整个工程的任务和资源无法统一调度。本系统在实现整个系统的高性能的同时，对任务调度进行抽象，封装出统一接口，实现对多个并行计算平台的任务和资源调度。
(hadoop,spark,hive,hbase, openmpi, mdcs)


* 人车绑定

在道路卡口外装小型基站，结合车牌识别系统(svm), 利用大数据分析实现手机与车辆的绑定(输入车牌号，找出可能在这辆车上的所有手机号)


### 0x0307 枪球联动

在公安三所实现的产品, 由枪机检测人脸,球机依据相应规则转到对应PTZ位置进行人脸检测、识别。
* 深度学习(caffe, alexnet, vgg)
* 最小二乘
* 图像增强
* 目标检测(Joint Cascade Face Detection and Alignment)

### 0x0308 计算机取证

介质读取,文件系统解析(FAT32, NTFS, HPFS, FAT32, ExtFat32), IM(QQ、阿里旺旺、飞信、Miranda等国内外即时通信软件)破解提取。








