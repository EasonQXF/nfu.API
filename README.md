# 20春API项目

|文档名称|Electronic-doctor—产品需求文档|
|--|--|
|产品名称|Electronic-doctor(电子医生)|
|产品描述|一款通过收集患者的饮食习惯、服药习惯等个人生活信息，运用人工智能技术(图灵机器人服务、高德地图API、人脸识别)进行数据分析整理并评估病人身体状态，协助规划日常生活的智能健康管理App|
|产品版本|1.0|
|文件现状|进行中|
|文件作者|丘小峰|

## 加值宣言
   我认为目前市面上欠缺可以对用户生活提供有效意见的提高用户的健康行为的健康智能管理类型App，虽然国内已有一些APP也开发了运动和饮食指导的功能，但这些指导难以为用户设计个性化方案，且缺乏深度的医疗价值。
   此款App能够给用户的健康生活行为提出专业可行的参考方案。通过图灵机器人服务，通过收集来用户个人信息的数据对用户提出意见，并且能与用户进行交流互动(文字或者语音)，语音识别将用户语音对话识别信息(语言类别等)交给机器人增加用户与App之间的交互体验，通过人脸识别将用户信息进行加密处理，使个人信息得到安全保障。用户可以将自身身体健康的数据分析结果在去医院就医时给医生就诊提供依据。并且有推荐系统，根据用户病情，通过高德地图API的路径规划、POI搜索推荐附近的医院或者药店、医生等。

## 一、需求概述
### 1. 产品背景
   直至目前，人们的生活中的健康素养还有待提高，特别是在庚子鼠年这场突如其来的新冠肺炎疫情中，虽然我国对疫情做出的措施有效抑制了疫情的持续散播，但是我们仍然要看到这场疫情中凸显出来的短板，此次疫情的传播之烈、防控难度之大，**从某种程度上反映出我国居民的健康素养尚有较大提升空间，而国民素养中很重要的一个环节就是培养健康的行为**。
### 2. 产品市场
现代年轻人很多都喜欢“朋克养生”，诸如用最贵的面膜，熬最长的夜，一边熬夜一边祈祷自己不要猝死；而老年人又缺乏医疗相关方面的知识，经常会听到又有老年人被骗去购买劣质保健品之类的新闻。这些都是不健康、不安全的行为，但是目前市场上并没有能够对人们身体状况信息进行整合评估的App，对于行动不便的老人或者是因为忙碌的工作的年轻人无法抽出时间去医院检查或者是咨询专业人士的意见的话，对于身体的状况就很难把握。现在为止我们的人工智能技术已经有了很大的发展，想要有一个移动的**医生机器人时刻关注自己的身体健康并提出专业意见会是一个不错的选择，并且机器人还能将数据通过授权分享给真正的医生，提供可靠的数据进行会诊**。
### 3. 市场概述
##### 3.1国内外智能健康管理类应用市场概述
- 国外健康管理类应用市场描述
> 由于医疗体系不同，发达国家的电子病历系统已接近完成，目前正在实施建设全国医疗信息化系统。1998年，英国国家医疗服务体系（NHS）提出为每位居民建立覆盖终生的电子病历并实现所有医生能访问这些电子病历，目前已基本完成。2010年，美国政府建立了国家健康信息网络（NHIN）， 即建立跨医疗机构的全国范围的电子病历，以此来实现医疗机构之间的信息共享。
                                       ——《国外健康类ＡＰＰ评价研究综述》-仝晶晶、邓胜利（武汉大学信息资源研究中心，武汉，４３００７２）
- 国内健康管理类应用市场描述                                       
> 国内的移动医疗目前缺乏类似日本的国家健康体系支持，商业化模式亦不完善，尚处于早期快速发展、快速“烧钱”与摸索阶段，准入门槛不高，产品良莠不齐，临床专业性App匮乏。根据中国APP客户端注册中心的数据显示，截至2014年，iTunes商店中已经有16275款医疗与健康相关的应用，主要集中在运动保健、自问诊平台和挂号预约，而在患者的用药提醒、病程记录和信息反馈方面基本处于空白状态。根据艾媒咨询发布的《2015年中国“互联网＋”医疗研究报告》，挂号预约类、问诊咨询类和医疗资讯类APP，分别占比28.5%、24.9%、17.9%，但这些APP大多功能有限，有的甚至只有1项主要功能，即提供相关的数据信息。这些APP内容同质化严重，有的应用看上去似乎更像是玩具。只有不到2500款应用既能够提供数据信息，又能够追踪用户的数据，至于拥有提示或预警等功能的应用数量就更少了。在这其中，预约挂号类APP受国内医疗资源分布的影响，过于集中在三甲医院，仅仅是提供资源的平台，而缺乏资源分流的能力。问诊类和咨询类APP由于线上咨询 和线下医疗的分离，大多只停留在初步问诊阶段，难以提供有效的医疗服务。而人们真正期待的革命性移动医疗应用应是能将常用功能成功整合到一个平台之上，而此整合后的平台又能够改善人们传统的保健与医疗方式。
          ——《健康管理类应用软件国内外现状与前景分析》 张子豪、章红英-首都医科大学基础医学院，北京-100069；首都医科大学中医药学院，北京-100069 
- 总结来看：
1. 国外健康管理类应用软件现状：国外健康管理类APP更多地结合了临床应用[4]，注重用药指导、临床指南、临床监测等功能的研发，为用户提供专业化、标准化的服务。
2. 国内健康管理类应用软件现状：国内健康管理类应用软件大多功能有限，有的甚至只有1项主要功能。人们真正期待的革命性移动医疗应用应是能将常用功能成功整合到一个平台之上。
因此产品发展动态：**如何将多个功能整合将是健康管理类APP设计和研发的重点，还要线上线下的同时开展，医疗器械、APP 应用、管理平台间的合作和整合将是未来行业发展的趋势。**
##### 3.2发展优势
- 目前健康管理里人工智能应用不多，有发展空间；
- 对健康管理类的需求，在线医疗的需求近年来，特别是在2020年新冠疫情期间需求增加；
- 将主流功能通过人工智能有机结合；
- “5G技术”逐渐普及，远程医疗成为了可能。

## 二、核心价值（最小可行性产品）
为用户的日常生活通过人工智能检测分析给出健康管理建议，并且数据可以提供给医生就诊时作为依据。
##### 用户痛点
1. 基层医疗资源分布不均匀，医疗专业人才缺乏；
2. 并没有能够功能齐全的一款App提供较为全面的医疗健康管理服务；
3. 以往的诊疗模式，无法支持医患间频繁的沟通。

## 三、用户分析
1. 目标用户群：
- 核心用户：基层用户，上班族白领等；
- 主要用户：能够使用智能手机的人群。

2. 用户画像及使用场景
![基层工人](https://gitee.com/EdisonQXF/API/raw/master/images/jicenggongren.png)
使用场景：经常干体力活，久而久之身体留下隐患，总会有一些暗痛，不知道怎么调理身体，也没有经济条件可以经常去看医生。于是使用这款电子医生App，能够很方便的知道自己最近的身体状况，并且知道具体怎么做的建议，比如饮食要怎么调整，做一些什么样的拉伸运动去缓解疼痛等等。
![上班族](https://gitee.com/EdisonQXF/API/raw/master/images/shangbanzu.png)
使用场景：“我希望能够生活得更健康，让工作轻松点。”我是一名典型的上班族 ，每天过着三点一线的生活，久而久之身体似乎比以前更容易疲惫了，工作的，忙碌得让我甚至没有时间去看医生。用这款App的话，人工智能可以像一个医生一样与我对话，让我在短暂休息的时候也能做一些健康运动，或者吃一些有益的食品，还能知道应该去看什么医生。

## 四、核心价值与用户痛点
|:--:|:--:|
|无法随时得到有价值的建议|通过图灵人工智能机器人根据用户数据智能分析并提出有效建议|
|无法知道应该去哪家医院好|通过高德地图api的路径规划进行推荐|
|个人资料信息的安全保证|通过人脸识别识别身份信息，使用信息需要授权

## 五、人工智能概率性与用户痛点
图灵机器人技术与高德地图开放平台的路径规划技术，有以下优势：

|图灵机器人技术优势/用户痛点|高德地图开放平台的路径规划技术优势/用户痛点|
|:--:|:--:|
|1. 语义理解准确：开放域聊天准确率81.64%，垂域技能准确率96.34%|1. 结合搜索方式：高德提供了千万级别的POI，通过POI搜索，可以完成找药店，找医院等等的功能|
|2. 知识图谱：千万级实体及关系知识，支持逻辑与关系的知识推理|2. 完善的地图数据系统：基于高德地图丰富的海量数据，呈现看病途径的地址信息、公交信息等|
|3. 基础知识库：问答知识库1亿条，高频知识库1000万条|3. 路径提示：用户得到相关信息推荐后可以进行相关搜索和筛选，多种不同方案路径规划方便用户|

所以，该产品利用图灵机器人进行科学分析得出解决方案，需要看病就医的情况下通过高德地图的路径规划结合POI搜索将可选择适合的医院、诊所告诉用户，让用户进行选择，并且规划出可行的路线，其中高德地图POI搜索的准确率较高，图灵机器人根据强大的数据库进行的分析出错率很低。

**识别、分析不准确的方法：机器自身的深度学习、丰富数据库**

## 六、需求列表（对应人工智能加值）
|序号|api技术|用户场景|优先级|
|--|--|--|--|
|1|图灵机器人|与用户进行对话（语音、文本）满足用户提出的需求|A（重要）|
|2|Azure 认知服务（如文本分析和语言理解）|来解释客户情绪和意图|A（重要）|
|3|Azure人脸识别|对用户个人数据进行保障的重要手段之一|A（次重要）|
|3|高德地图API的路径规划|寻找并推荐合适条件的医生、医院、药店等信息给用户|B（次重要）|

## 七、产品结构图（图片可能比较大，加载不出来刷新即可）
1. 产品功能结构图
![产品功能结构图](https://gitee.com/EdisonQXF/API/raw/master/images/%E4%BA%A7%E5%93%81%E5%8A%9F%E8%83%BD%E7%BB%93%E6%9E%84%E5%9B%BE.png)


2. 用户流程图
![用户流程图](https://gitee.com/EdisonQXF/API/raw/master/images/%E7%94%A8%E6%88%B7%E6%B5%81%E7%A8%8B.png)


3. 产品结构图
![产品结构图](https://gitee.com/EdisonQXF/API/raw/master/images/%E4%BA%A7%E5%93%81%E7%BB%93%E6%9E%84%E5%9B%BE%20(1).png)

## 七、数据推理
||页面|
|--|--|
|问题1|我们在页面上可以获得什么内容|
|回答1|身体情况分析可视化表格、症状可能分析结果、推荐饮食、运动、治疗方案|
|问题2|向用户输出的结果内容从哪里来|
|回答2|建立数据库和去开放平台调用api，进行智能分析获得结果内容|
|问题3|请求从哪里来|
|回答3|用户或者智能设备对产品输入身体状况的相关信息|
|问题4|如果分析病情的过程中出现明显的识别错误，应该如何获取并处理这些数据数据|
|回答4|通过用户的反馈功能进行信息获取，通过用户的自愿反馈扩大数据库，强化机器学习，不断扩大数据库进而降低失败率|

## 八、产品原型及交互设计

## 九、API的运用（展示主要应用API）
**需要通过注册登录得到API Key和Secret Key获取access_token**
###### （一）路径规划
文档参考地址：[https://lbs.amap.com/api/webservice/guide/api/direction](https://lbs.amap.com/api/webservice/guide/api/direction)
![路径规划](https://gitee.com/EdisonQXF/API/raw/master/images/%E4%B8%AD%E5%8C%BB%E5%8C%BB%E9%99%A2%E8%B7%AF%E5%BE%84%E8%A7%84%E5%88%92.png)

###### （二）图灵机器人
```python
def tuling(msg):
    api_key = "******"
    url = 'http://openapi.tuling123.com/openapi/api/v2'
    data = {
        "perception": {
            "inputText": {
                "text": msg
            },
        },
        "userInfo": {
            "apiKey": api_key,
            "userId": "1"
        }
    }
    datas = json.dumps(data)
    html = requests.post(url, datas).json()
    if html['intent']['code'] == 4003:
        print("次数用完")
        return None
    return html['results'][0]['values']['text']
msg = '我今天肚子疼'
print("原话>>", msg)
res = tuling(msg)
print("图灵>>", res)
```
输出：
原话>> 我今天肚子疼
图灵>> 等等哦我帮你看看是怎么回事

**图灵机器人API和青云客智能聊天机器人API的比较**
|      | 图灵机器人API                                                                                                                                                        | 青云客智能聊天机器人API                                                                                            |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 功能 | 开放域聊天准确率81.64%，垂域技能准确率96.34%  知识图谱：千万级实体及关系知识，支持逻辑与关系的知识推理；多轮对话：开放域聊天与垂域技能超过5轮的上下文对话能力 | 天气、翻译、藏头诗、笑话、歌词、计算、域名信息/备案/收录查询、IP查询、手机号码归属、人工智能聊天 |
| 价格 | 需要注册账号，可以申请5个机器人，未认证账户每个机器人只能回3条/天，认证账户每个机器人能用100条/天。 | 完全免费！不用注册，不用申请key，拿来就用！|
| 体验感受 | 回答准确率高，交互体验良好 | 功能单一，体验不良|

## 十、API的使用价格
1. 图灵机器人
需要注册账号，可以申请5个机器人，未认证账户每个机器人只能回3条/天，认证账户每个机器人能用100条/天。

2. 高德地图API
![高德地图API](https://gitee.com/EdisonQXF/API/raw/master/images/%E9%AB%98%E5%BE%B7%E5%9C%B0%E5%9B%BEAPI%E6%8A%A5%E4%BB%B7.png)

## 十一、API使用风险评估
本产品需要收集用户的个人信息，例如身体状况、指标等，这些数据属于个人十分隐私的数据，然后再通过人工智能数据分析等操作。这些数据需要得到足够的安全保障。可以在建立数据库的时候加入区块链技术也可以通过加密用户数据，使用的时候需要得到用户的授权，比如输入用户个人身份证号、人脸识别等。

## 十二、竞品分析
1. 竞品对象——春雨医生App

2. 竞品的战略定位分析
春雨医生搭建了自诊和问诊系统，定位于用户的诊前咨询，主要解决用户在“身体不适”到“去医院”之间的需求，这被春雨医生定义为“轻问诊”。

3. 竞品的产品结构
![春雨医生](https://gitee.com/EdisonQXF/API/raw/master/images/%E6%98%A5%E9%9B%A8%E5%8C%BB%E7%94%9F.png)

4. 竞品的差异化分析
 4.1 区别
- 春意医生竞品：春雨医生主要是通过大数据的方式分析病情只分轻度的和严重的，轻度给出基本建议，严重的病情会练习在线医生，与医生进行线上沟通。这是春雨医生主打的“轻问诊”模式。

 4.2 缺点
- 问诊类和咨询类APP由于线上咨询和线下医疗的分离，大多只停留在初步问诊阶段，难以提供有效的医疗服务。

**结论：相比春雨医生，我们的Electronic-doctor(电子医生)产品加入了人工智能，结合大数据的数据分析、数据可视化可以提供更权威的数据分析结果，并且能够为用户得到推荐治疗方案后的路径规划等提供良好的用户体验。春雨医生的“轻问诊”我们可以学习，加入在线医生问诊的功能，并且在此基础上不断完善。**

## 十三、该产品未来的发展路线构想
定好产品的主要发展功能、领域，然后不断完善，基础到成熟，之后再逐渐发展附属功能，最终成为一个成熟的产品。

#####  (一）产品的更新迭代过程
- **V1.0**
   1. 实现人工智能机器人功能，满足基本的智能操作、交流需求；
   2. 实现高德地图路径规划功能，满足用户的交流需要；

- **V2.0**
   1. 人工智能数据库逐渐完善减少失误率；
   2. 增加在线预约门诊、医生预约等功能；
   
- **V3.0**
   1. 人工智能数据库完善趋向成熟，几乎没有失误率；
   2. 产品用户流量增多，根据用户需求完善周边附属功能；

#####  (二）产品可能涉及的功能范围
- 在线智能机器人根据用户数据分析病情，给出治疗方案
- 用户选择治疗方案的时候有高德地图API为其进行路径规划、导航等
- 医生在线问诊，通过审核的医生会在线解答病患病情

#####  (三）产品的盈利模式
1. 广告盈利
> 本小程序是医疗健康类小程序，后期成熟后可以招募药店、医院、医学院等相关医疗机构、医疗教育行业的广告，从中获得广告费盈利。
2. 平台入驻盈利
> 前期做好宣传，可以选择邀请友商入驻，利用大的流量ip吸引用户，初定为免费的不收费，待到成熟，有一定的流量、知名度、访问度之后可以向入住的平台收取摊位费、推广费等。
3. 发展周边
> 我们可以选择发展医疗周边，可以是友情赞助商提供的医护用品，例如口罩、棉签等等。待到资金到达一定的程度，我们可以选择发展自己的ip，并利用其流量和知名度做成周边商品，吸引用户进行购买，从而获得资金收入。
4. 增加付费的高端项目
> 我们还可以为高端人群客户定制化服务，在保障普通用户的正常使用功能外，再开发更高端的服务，吸引特定的人群进行升级服务，消费升级。

#####  (四）产品的业务模式
![业务模式](https://gitee.com/EdisonQXF/API/raw/master/images/%E4%B8%9A%E5%8A%A1%E6%B5%81%E7%A8%8B.png)

### 所使用的API功能链接
- [高德地图API](https://lbs.amap.com/api/webservice/guide/api/direction)
- [图灵机器人](http://www.turingapi.com/scene)
- [Azure认知服务](https://azure.microsoft.com/zh-cn/services/cognitive-services/)

#### 一句话版本
现代人们生活的节奏越来越快，医疗资源仍然存在分配不均匀的情况，人们需要这样一款能够随时随地进行数据分析整理并评估病人身体状态，协助规划日常生活的智能健康管理App。通过人工智能技术的结合：智能机器人、路径规划等等，解决像基层工人、上班族这样的没时间或没经济能力的人群的健康需求。
#### 1分钟版本
现在国内外都有很多的健康管理类App，特别是受2020年疫情的影响，更是掀起了热潮。但是功能都比较单一，将功能进行有机结合的产品并，没有。
![健康管理App](https://gitee.com/EdisonQXF/API/raw/master/images/App%E8%81%9A%E5%90%88.jpg)
所以本产品是通过AI人工智能技术将产品功能有机结合。图灵机器人能够与用户进行对话（语音、文本）满足用户提出的需求，加入Azure 认知服务（如文本分析和语言理解）来解释客户情绪和意图 。通过高德地图api的路径规划、POI搜索寻找并推荐合适条件的医生、医院、药店等信息给用户。还可以加入门诊预约、在线医生等主流功能。让用户享受全方位、可行性高的健康管理服务。还可以通过知识付费、广告周边等方式获得收入盈利。
