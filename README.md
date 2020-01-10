# APP：“云游四方”
[40x40秒的带narration 语音口白的Powerpoint ](https://github.com/xinqi3050/wandering_around/blob/master/%E4%BA%91%E6%B8%B8%E5%A4%A9%E4%B8%8B.pptx)
# Product Requirements：产品需求

Title | content
---|---
Target release(发布日期) | 2019/11/25
Epic(史诗名称) | 云游四方（我的云导游APP）
Document status(文档状态) | 已完成
Document owner( 文件的主人) | [林新棋](https://gitee.com/xinqi3050)
Designer( 领头的设计师) | [林新棋](https://gitee.com/xinqi3050)
Developer( 领头的开发者) | [林新棋](https://gitee.com/xinqi3050)
QA(领头的测试者) | [林新棋](https://gitee.com/xinqi3050)

# 价值主张设计
## 加值宣言
>  一款旅游景点解说app，主要运用百度的语音合成，语音识别和高德地图的人工智能API，帮助喜欢自由行的用户在景区旅游的时候提供景点解说功能，充当云导游的角色，让用户的旅程充满有趣的知识和故事。

## 核心价值
>  短语音识别：将60秒以内的语音精准识别为文字，可适用于手机语音输入、智能语音交互、语音指令、语音搜索等短语音交互场景
   语音合成：基于业界领先的深度神经网络技术，提供高度拟人、流畅自然的语音合成服务，让您的应用、设备开口说话，更具个性
   高德地图：支持识别约12万中外著名地标、景点，广泛应用于拍照识图、图片分类等场景

## 价值主张
###  一句话版本：
> 实时解说，做你身边的云导游
### 一分钟版本
> 云游四方主要运用百度的语音合成，语音识别和高德地图的人工智能API，帮助喜欢自由行的用户在景区旅游的时候提供景点解说功能。以语音合成为基础功能，应用于移动旅游景点解说场景，用户可以通过语音识别识别用户的关键词为用户提供旅游景点的相关介绍和在网上使用搜索引擎搜索有趣的故事，用语音合成播放给用户听。用户也可以通过上传照片，使用图像识别上传当地的标志性建筑物，软件将为用户讲述建筑的历史和有趣故事。

## 目标用户
适用人群 | 旅游行为特点 | 其他
----|----|----
年轻旅游群体 | 大部分会选择自由行/结伴旅游，旅游行程自由度高 | 对旅游景点的地理知识/人文故事感兴趣
自由职业者 | 大部分会选择来一场说走就走的旅行，不受拘束 | 对未知旅游景点的好奇心强，希望结交兴趣相投的好友

## 用户痛点
- 对当地的旅游景点缺乏认知，也缺少了解的系统渠道，想知道更多的旅游景点的信息
- 用户使用搜索引擎得到的词条资料介绍过于机械生硬，不适用于旅游情境，游客一般不会在旅游时查看
- 来到未知的旅游目的地，不知道附近有什么有趣的旅游景区可供即时选择
- 用户在旅游过程很无聊，希望听到关于旅游景点的有趣故事

 ## 背景故事
 - 国内市面上大部分旅游出行类软件功能都大同小异：提供出行资讯、衣食住行等硬件服务，或者充当旅游行程助手（如携程旅行、马蜂窝旅游、飞猪、爱彼迎等），这类功能的软件市场已经比较饱和，竞争也大。
 - 极少具有人文科普功能的旅游出行类软件。马蜂窝旅游虽然也有对部分景点加以介绍，但因为虽然主打旅游攻略，因此其介绍的内容不深入。
 - 搜索引擎的词条资料介绍过于生硬，不适用于旅游情境，旅游出行者都不会在旅途中主动、零散地搜索/阅读相关景点科普。
 - 所以国内自助导游类/具有旅游解说功能的旅游出行软件在市场上有很大的空白，代表性产品缺少（三毛游app、链景旅行app等软件的知名度不高）。

## 人工智能概率性与用户痛点
- 百度的地标识别api采用的是细粒度图像识别 (fine-grained image recognition)，即**精细化分类**。
- 识别出物体的大类别（比如：花、草、狗等）较易，但比如区分月季和玫瑰，判断更为精细化的物体分类名称，则难度极大。最大的挑战在于，同一大类别下不同子类别间的视觉差异极小。
- 因此，精细化分类需要更高的图像分辨率。百度细粒度图像识别目前支持动物、植物、菜品、地标等，能精准识别超过十万种物体和场景，包含多项高精度的识图能力并提供相应的API服务。
- 地标识别现在对上传图片场景的清晰度较高，模糊度较高的情况下较难识别。
- 对于最新、最近完工的建筑，暂时无法识别。但对于用户来说，旅游往往会选择历史年份较久的建筑，所以此类情况忽略不计。

## 需求列表与人工智能API加值
用户故事 | 重要性 | 备注 | 人工智能API加值
----|----|----|----
 我不想在游览 景点的时候看手机文章，但是同时我也想了解 | 非常重要 | 文章正文具有语音朗读功能，并且能后台播放 | [百度AI_语音技术_语音合成](http://ai.baidu.com/tech/speech/tts)
 到达旅游目的地后，我想了解附近景点的相关开放信息和景点故事| 非常重要 |定位当前位置，点击地图上显示的标记地点查看相关资料 | 1、[高德地图_Web服务_搜索POI](https://lbs.amap.com/api/webservice/guide/api/search/#scene)搜索景区；2、 [高德地图_隐藏地图上的文字标注](https://lbs.amap.com/dev/demo/map-text#Android)和[高德地图_多信息弹窗/气泡效果](https://lbs.amap.com/dev/demo/multiple-infowindows#Android)将应用到景点地图页，显示景区地图全景的时候会标记里面每一个景点，隐藏文字标注，放大地图后会有一个小的信息弹窗，用户可以直接点击语音播放标记播放经典故事，也可以点击弹窗浏览文字内容；3、 [高德地图_地图选点](https://lbs.amap.com/dev/demo/place-choose#Android) [高德地图_地点查询](https://lbs.amap.com/dev/demo/place-search#Android) 应用于用户浏览景区地图时查找某个景点的解说语音：用户可以在景区内输入景点关键字搜索，点击返回结果就能在景区定位该景点
 
----- 

## 交互及界面设计
- #### 产品结构思维导图
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E4%BA%A7%E5%93%81%E7%BB%93%E6%9E%84%E6%80%9D%E7%BB%B4%E5%AF%BC%E5%9B%BE.png)
- #### 部分API调用流程示意图
1. 语音合成API（以语音解说景点为例）
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E8%AF%AD%E9%9F%B3%E5%90%88%E6%88%90api%E8%AF%B4%E6%98%8E%E5%9B%BE.png)
2. 地标识别API（以搜索景区地图内景点为例）
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E5%9C%B0%E7%82%B9%E6%9F%A5%E8%AF%A2.jpg)

## 产品原型展示

### [原型文档查看](http://xinqi3050.gitee.io/travel-around-prototype)
### [原型文档下载](https://github.com/xinqi3050/Travel-around-prototype)

### 产品原型展示

- 百度语音识别API：在主要功能页中，按住说话按钮就可使用到。
- 百度语音合成API：在主要功能页中，按住语音播放按钮就可使用到。
- 百度地标识别API：在主要功能页中，点击拍照功能就可使用到。

                       首页                                                    主要功能页
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E5%8E%9F%E5%9E%8B1.jpg)
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E5%8E%9F%E5%9E%8B2.jpg)

                       旅友                                                      我的
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E5%8E%9F%E5%9E%8B3.jpg)
![image](https://github.com/xinqi3050/wandering_around/blob/master/%E5%8E%9F%E5%9E%8B4.png)

### 口头操作说明
> 首页可以查看搜索次数最多，用户评论最多的景区，用户也可以通过搜索框查找自己想要的景区；轮播图会展示热搜榜前三的景区；
推荐列表功能会根据用户的地理位置推荐用户最佳的旅游景点；旅游要记有大量的旅游事迹文章，可供用户参考旅游事宜。

> 主要功能页可以向用户展示当前位置，以及景区的内部地图，用户可以在景区内查找建筑物；用户可以使用地标识别，找出景区内的相关故事，并通过语音播放功能在旅途中感受景区的文化，用户也可上传图片找到地标图片中的相关故事，并播放语音。
  
> 驴友页可以让用户在旅行过程中结交新的朋友，也可以向朋友展示自己当前的旅游景区。
  
> 我的页面可以自由设置软件主题风格，语音播放速度等功能。
## API输出入展示
[百度API产品说明文档](https://ai.baidu.com/ai-doc/SPEECH/Gk38y8lzk)
> ### 测试百度语音合成rest api识别接口流程
### 修改tts.py

从网页中申请的应用获取appKey和appSecret

```python
API_KEY = 'IXs36fIdZVfPHLh7hDtNmF45'

SECRET_KEY = 'jBF1BPkHDHH2jvQRXPmakSMFCtB5zyCd'
```

### 运行 tts.py，进行合成

命令为 python tts.py

结果在result.mp3，如果遇见错误，结果在error.txt

其中

- Content-Type: audio/mp3，表示合成成功，可以播放MP3 result.mp3
- Content-Type: application/json 表示错误   error.txt打开可以看到错误信息的json


### 修改合成参数

```
TEXT = "欢迎使用百度语音";

#发音人选择, 0为普通女声，1为普通男生，3为情感合成-度逍遥，4为情感合成-度丫丫，默认为普通女声
PER = 0;
#语速，取值0-9，默认为5中语速
SDP = 5;
#音调，取值0-9，默认为5中语调
PIT = 5;
#音量，取值0-9，默认为5中音量
VOL = 5;

CUID = "123456PYTHON";

```
> ### 百度语音合成API的Python调用代码
[→ 点击此处查看](https://github.com/xinqi3050/wandering_around/blob/master/tts.py)


> ### 高德地点查询
- 配合输入提示功能使用，提升 POI 搜索的用户体验：根据输入提示功能返回的提示词，若提示词的 id  为空，说明该提示词不是 POI，需以该输入词为关键词进行 POI 搜索，查询具体的地点；若 id 不为空，则是真实存在的地点，直接可以在地图上展示。
```
<code class="java hljs"><span class="hljs-meta">@Override</span>
<span class="hljs-function"><span class="hljs-keyword">protected</span> <span class="hljs-keyword">void</span> <span class="hljs-title">onActivityResult</span><span class="hljs-params">(<span class="hljs-keyword">int</span> requestCode, <span class="hljs-keyword">int</span> resultCode, Intent data)</span> </span>{
    <span class="hljs-keyword">super</span>.onActivityResult(requestCode, resultCode, data);
    <span class="hljs-keyword">if</span> (resultCode == RESULT_CODE &amp;&amp; data
        != <span class="hljs-keyword">null</span>) {
        mAMap.clear();
        Tip tip = data.getParcelableExtra(Constants.EXTRA_TIP);
        <span class="hljs-keyword">if</span> (tip.getPoiID() == <span class="hljs-keyword">null</span> || tip.getPoiID().equals(<span class="hljs-string">""</span>)) {
            doSearchQuery(tip.getName());
        } <span class="hljs-keyword">else</span> {
            addTipMarker(tip);
        }
    }
```

> ### 高德地图多信息弹窗/气泡效果
```
aMap.setOnCameraChangeListener(new AMap.OnCameraChangeListener() {
        @Override
        public void onCameraChange(CameraPosition cameraPosition) {

        }

        @Override
        public void onCameraChangeFinish(CameraPosition cameraPosition) {
            if (!isItemClickAction) {
                locationMarker.setPosition(cameraPosition.target);
            }
        }
    });
```

## API使用比较分析
> - ### 百度的语音合成API：
- 语音识别、合成接口调用量无限。
- 语音合成指定某个字的发音：语音合成接口，支持自主标音，通过在所需合成的文字后，增加音标的方式，比如，想把“重音”中的重字，指定合成"chong"的读音时，需将合成文字改为“重（chong2）音”，其中2表示2声，可以根据数字变化调节音调，1对应1声，2对应2声，3对应3声，4对应4声。
- 语音合成目前支持中文普通话播报、中英文混读播报，音色支持男声、女声、度丫丫、度逍遥。
- 支持离线在线融合模式:SDK可以根据当前网络状况，自动判断使用本地引擎还是云端引擎进行语音合成，断网情况下也可继续使用。
- 不过合成文本长度必须小于1024字节，如果本文长度较长，可以采用多次请求的方式。文本长度不可超过限制。

> - ### 高德地图&百度地图

比较内容|百度地图API|高德地图API
---|---|---
是否免费|免费|免费
定位功能|百度智能定位服务帮助广大开发者更好解决"你在哪里这个难题；支持GPS、WiFi、基站融合定位；完美支持各类应用开发者对位罝获取的诉求|高德地图定位通过GPS定位，基站定位，混合定位三种定位模式为用户提供高精度的定位服务，开发者可以通过获取用户位置，设置地理围栏，实现高精度推送，通过用户分布合理布詈资源：实现效益最大化。
地图功能|帮助用户轻松实现全平台地图展示；支持3D高清地图、全景图、实时路况图、静态图；自定义个性化地图样式，打造专属地图；|高德开放平台提供2D, 3D,卫星多种地图形式供开发者选择，无论基于哪种平台，都可以通过高德开放平台提供的API和SDK轻松的完成地图的构建工作。同时我们还提供强大的地图再开发能力，全面的地图数据支持，离线在线两种使用方式，多种地图交互模式，满足各个场景下对地图的需求。
数据服务功能（搜索）|提供位罝描述、地点检索、地址解析、推荐上车点等数据服务；百度&用户隐私地理数据融合，满足个性化数据 使用需求分析；|为用户提供基于地理位罝的搜索功能， 如地点关键宇搜索，周边附近搜索，多边形范围内搜索，地点与坐标点之间 的正逆地理编码搜索，以及搜索输入提示，天气查询等常见搜索功能。|

### 所以从开发角度评估地图API 易用、稳定、效率、业务支持的话：
- 易用性、稳定 高德地图API > 百度地图API
- 业务支持 百度地图API > 高德地图API
- 综合能力高德地图比百度地图专业精准，所以选择使用高德地图API


## 问题
问题（如何让用户了解这个特性） |  结果（沟通已达成的决定）
---|---
用户发现地图上的景点开放信息/景点故事有误 | 用户可以在景区地图界面右上角点击反馈，提交反馈后系统会提醒用户继续享受旅程，并告知用户后台会审核用户的反馈信息
非管辖旅游地/非景区旅游地搜索不到 | 搜索页面显示：未找到含“xxx”的景区/城市
没有国外的旅游景区解说 | 待完善其他国家和地区的旅游景点资料

## 可选方案/产品改版方向
- [ ] 可添加用户旅游足迹的标记
- [ ] 旅游景区的推荐路线
- [ ] 景点观景拍摄点推荐
- [ ] 语音包定制、付费功能
- [ ] 增加社交功能
- [ ] .....

## 清单
### [原型文档查看](http://xinqi3050.gitee.io/travel-around-prototype)
### [原型文档下载](https://github.com/xinqi3050/Travel-around-prototype)
### [百度API产品说明文档](https://ai.baidu.com/ai-doc/SPEECH/Gk38y8lzk)
### [Python调用代码](https://github.com/xinqi3050/wandering_around/blob/master/tts.py)
