# **个人简历**

## 个人信息

-|- 
-|-
姓名: 许友正|出生年月: 1984.12
教育背景: 2005-2009山东大学物理, 本科|手机: 15759268138
邮箱: xuyouzhengzhenghe@126.com|居住所在地: 厦门同安
github: [https://github.com/oylz](https://github.com/oylz)|-

## 技能/优势
* 16年c++经历,擅长linux编程、性能优化、疑难问题排查
* 10年cv经验:
    * 行业:人脸检测跟踪识别、车牌识别、工业异常检测
    * 领域:图像分类、目标检测、图像分割、深度估计、关键点匹配
* 5年nlp经验:词向量、文本分类、命名实体、句法分析、llm微调
* 10年java及python经历
* 熟悉DL框架上训练及推理
    * tensorflow、torch、caffe、tensorrt、rknn(npu)
    * vllm、llama.cpp、ollama、transformers
* 擅长模型加速及精度优化: onnx转换、模型调优
* 开源社区积极参与者
    * [openpose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)贡献者
    * [M-3LAB](https://github.com/M-3LAB/awesome-industrial-anomaly-detection)贡献者
    * 贡献项目[DS](https://github.com/oylz/DS): 具有深度关联度量的在线多目标实时跟踪
    * 多个项目issue的积极解决者[GroundingDINO](https://github.com/IDEA-Research/GroundingDINO/issues/156#issuecomment-2324608395)、[transparent-background](https://github.com/plemeri/transparent-background/issues/13)、[BFSR](https://github.com/liyuantsao/BFSR/issues/1)、[dinov2](https://github.com/facebookresearch/dinov2/issues/19)
    * 贡献两个分割模型:gound.onnx、inspyrenet.onnx, 下载数1000+ 

## 工作经历

* 智业互联: AI部门经理, 2020.04-2024.11
    * 人工智能,数据中心,架构设计,疑难排查
    * 2023智业软件技术创新奖,2022智业健康产研中心特别荣誉奖
* 厦门亿联: teamleader, 2018.02-2020.01
    * 架构设计,基础组件,链路追踪
    * 股权激励对象
* 深图智服: 技术架构师, 2017.03-2018.01
    * 人脸检测识别,多目标跟踪,视频编解码
* 网宿科技: 架构师, 2016.07-2017.03
    * 50万并发接入服务,异地双活
    * 2016网宿技术创新奖
* 公安三所: 技术主管, 2013.03-2016.06
    * 大数据,车牌识别,人脸识别,相机标定
    * 2014公安部三所技能大赛三等奖,2013公安三所优秀员工
* 盘石软件: c++主程, 2009.04-2013.03
    * 计算机取证
    * 2011盘石软件上海优秀员工


## 主要项目经历

### 1.个人助手+数字人
* 项目介绍:个人助手旨在指导用户完成功能辅助(预约挂号、分诊叫号、充值、购药等)、智能菜单导航(分诊叫号、报告查询等)、知识问答(问药、问病、指标百科等),具备多场景切换能力.并兼数字人化身实时播报.
* 职责:项目负责人兼架构设计、选型、算法、主程
* 技术
    * 场景识别、槽位抽取: llama-3.1,qwen-1.5
    * 文本转语音、声音克隆: fishspeech-1.5
    * 文本向量: acge_text_embedding
    * 数字人: echomimic,sadtalker
* 成果: 已在厦大附属第一医院app上线,其中数字人可以做到每秒60帧的生成速度

### 2.智能导诊+预问诊
* 项目介绍:根据用户输入的疾病或症状,从知识库中检索最匹配的主体,追问相关症状、程度、时长等属性,最后向用户推荐就医科室,如果是预问诊场景则直接生成预问诊病历.
* 职责:项目负责人兼架构设计、选型、算法、主程
* 技术:
    * 属性抽取:llama-2,高斯混合聚类
    * 文本向量: simbert
* 成果: 已在全国几十家医院app上线,并收到用户的反馈在不断完善中

### 3.报告单识别
* 项目介绍:根据用户上传的检查检验报告单图片,识别出报告单名称、指标数据(名称、数值、参考范围)
* 职责:选型、算法、主程、优化
* 技术:
    * 文档分割: sam
    * 文档扭曲矫正: doctr-plus
    * ocr: paddleocr文本行检测,读光ocr文本识别
    * 表格识别: 读光无线表格识别
    * llm总结: qwen-1.5
    * 速度优化: onnx,tensorrt
* 成果:
    * ocr速度由每张1.9秒优化到190ms
    * ocr精度由99.5%提升到99.93%
    * 表格识别精度提升到业内前沿水平(与合合的表格识别比较)

### 4.智能拍照系统
* 项目介绍:系统自动检测初拍照者的头发、坐姿、眼睛、脸部、衣服信息,指导其完成相应动作,拍一张符合身份证标准的照片,并裁剪成标准身份证照.
* 职责:架构、选型、算法
* 技术:
    * 人脸检测: retinaface
    * 人脸关键点: landmark106, mediapipe
    * 人脸分割: farl,face_parsing,self-correction-human-parsing
    * 人物衣着: fashion_analyze,fashionformer
    * 人体姿势: human_pose
    * 人脸姿势: synergynet, spiga
    * 清晰度: topiq_nr_face
    * 表情识别: emotion
    * 口罩检测: mask360
    * 背景去除: modnet
    * 视频流: ffmpeg
* 成果: 已在福建省泉州市丰泽区公安局上线

### 5.拉链缺陷检测
* 项目介绍:检测拉链上的缺陷区域,与产线结合自动质量检测.
* 职责:架构、选型、算法
* 技术:
    * 部件分割: segformer,deeplab-v3
    * 缺陷检测:destseg,diffusionad,glass,uniad
* 成果:
    * 精度: image_auc-roc 99.3%, pixel_auc-roc:99.6%
    * 速度: 300ms/frame
    * 已在福建省晋江市某厂投入使用

### 6.其它
* 身份证户口本识别
* 智能评估
* 药品ocr+以图搜图
* 身份证照片质量检测
* 数据库限流基础组件
* fullgc线程栈抽取组件
* 宁德、龙岩核酸系统性能优化
* 数据中心
* 应用性能管理
* 数据同步组件
* IM/推送服务
* 智能安防
* 连麦
* 高性能并行计算集群
* 人车绑定
* 枪球联动
* 计算机取证









