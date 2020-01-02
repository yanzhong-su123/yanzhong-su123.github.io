<div align="center">
  <h1>:whale2: 项目名称：Fun_photo :whale2:</h1>
  <p>基于Baidu & face++的API所设计的Fun_photo APP</p>

</div>


> PRD 价值主张设计（不同场景适用不同版本）
> 1. 一句话版本<br>
    此款 **Fun_photo** APP 通过调取 **图像处理的相关api** ，用户只需将本地照片上传，本产品会帮助你自助识别图中的场景并反馈结果，为用户提供快速抠像并进行美颜，同时还可以继续二次创意创作（图片风格置换）...待完善
> 2. 一分钟的版本 (图文线上可阅读含可查链接)<br>
    这款 **Fun_photo** 产品，通过调用 **Baidu** 图像处理中的 **图像技术** ，包括**通用物体和场景识别api**、**图像风格转换api** 模块，另和 **Face++** 中的 **人体识别、人像处理** ，包括**人体抠像api**、**人脸美颜api** 模块，可以帮助用户识别旅游场景中出现的物体和搜索其对应的百科信息，同时可以为用户提供人物抠像和美颜，用户可以根据自己的需要是否继续二次创意创作（抠像成功后的风格置换）。该产品是基于市面上缺乏一些让用户对图片进行二次创作的软件、**查询图片的内容时间成本较高** 和**二次创作过程较为复杂**的用户痛点下，推出**“一系列图像处理”**的模块产品，并绘制**最小可行性产品原型**，来为用户提供更加便捷的图片创作和内容查询的功能服务。
    设计一款即可以帮助用户识别旅游场景中出现的物体和搜索其对应的百科信息，又可为用户提供人物抠像，也可以对抠图后的人像进行二次创作（图片风格置换），增强用户的创作性和其中的趣味感。
> 3. [400 秒版本 Pecha Kucha 20x20 版本]() (线上投影片含可查连结)<br>

# ✨Product Requirement（产品说明文档）
---

|  发布日期 | 2019-12-10 |
 | -- | -- |
 |  名称 | Fun_photo |
 |  文件现状 | 进行中 |
 |  文件的主人 |  苏衍中|
 |  领头的设计师 | 苏衍中  |
 |  领头的开发者 |  苏衍中 |
 |  领头的测试者 |  苏衍中 |
 
 # ✨Catalogue（目录）
 |产品的PRD设计|原型设计|机器学习之API的输出入展示
|---------- | --- |---------- 
|[PRD1-加值宣言](#chapter1) |[产品功能架构](#chapter14)|[API输入与输出](#chapter18)
|[PRE2-核心价值](#chapter2) |[流程图](#chapter15)|[API1.使用水平](#chapter19) 
|[PRD3-用户痛点宣言](#chapter3) |[全局说明](#chapter16)|[API2.使用比较分析](#chapter20)
|[产品简介](#chapter4) |[原型1.交互及界面设计](#chapter17) |[API3.使用后风险报告](#chapter21) 
|[产品背景](#chapter5) |[原型2.信息设计](#chapter17)|[API4.加分项](#chapter22)
|[产品目标](#chapter6) |[原型3.原型文档](#chapter17)|---------- 
|[用户画像](#chapter7) |[Axure交互及设计高保真原型](#chapter17) |---------- 
|[用户需求](#chapter8) |[原型4.口头操作说明 ](#chapter17)|---------- 
|[情景假设](#chapter9) | --- |---------- 
|[问题与解决](#chapter10) | --- |---------- 
|[考虑后不完成之项](#chapter11) | --- |---------- 
|[PRD4-人工智能概率性与用户痛点](#chapter12)| --- |---------- 
|[PRD5-需求列表与人工智能API加值](#chapter13)| --- |---------- 

# 一、产品说明

## ⭐️PRD1.加值宣言
通过运用通用物体和场景识别api，让用户快速查找到图片相关的更多内容，增强用户的体验度。
通过运用人体分割api和人脸美颜api来识别出图像中人体的轮廓范围，与背景进行区分，并返回所抠的图人像，帮助用户快速实现一键抠像，在抠图的过程中可以勾选美颜效果，提高用户“抠像＋美颜”的实现效率。
运用图像风格转换api可简单地将图像换成不同的风格，实现用户对图像的二次趣味创作。

- 实用简便性：通过简单的拍照或上传图片即可查询到图片的更多信息，反馈图片的内容和一些百度百科的超链接，便于用户对场景的更多了解。
- 趣味创作性：用户可对于自己的照片进行一键抠图，同时还可以对自己所抠的人像进行风格置换，创作出有趣的、有个性的图片。

## ⭐️PRD2.核心价值
基于用户的最基本需求，本产品提供图像场景识别的信息反馈的功能服务，为用户提供便捷的（抠图+美颜）功能，并对所抠的人像进行二次创作（图片风格置换），从而实现抠图后的创意创作。

## ⭐️PRD3.价值策略
- 针对目前的图像处理软件功能较为齐全和强大，在此方面本产品的竞争优势相对较弱，但本产品主打简洁明了的操作界面、只需上传图片和简单几步既可实时场景的识别并反馈信息，也可对抠像后的人像进行二次创作，通过置换图片风格与所扣的人像结合，可实现人物形象的风格多样化，增强本产品的趣味性，并且也可减少用户在创作过程中的时间成本，有效地提高用户的参与度。

*下面是用户调查与细分

# 背景：
> 当前市面上图像处理软件众多，其功能更多的侧重于对图片的处理，但缺乏一些让用户对图片进行二次创作的软件，同时当用户希望对当前的场景或本地图片有更多的了解，却发现较难的搜索到图片的相关内容，查询更多内容的时间成本较高。因此本产品希望通过简单的操作即可实现用户上述缺乏的功能，高效地实现用户二次创作和查询图片信息并反馈。

# 目的：
  设计一款让用户可以简单操作几步即可实现查询图片信息的更多内容并得到百度百科的链接反馈、有效率地实现图像背景与人像的分割、对人像图片进行风格置换，增强用户对本产品的体验好感。

# 目标用户：
年龄：18-35岁的社会年轻群体
性别：无限制
用户特征：喜欢使用图像处理软件但又嫌弃其操作过程较为复杂、对生活充满活力，敢于和愿意尝试不同的新事物。

> 用户画像:

# 用户调研：访谈法（8人）
*主要问题

1. 你平时有使用图像处理软件或app的习惯吗？
2. 你对于一款具有查询图片信息的更多内容、有效率地实现图像背景的置换和人物抠像的融合功能的软件感兴趣吗？
3. 你所拍的照片一般会用于二次创作吗？
4. 您曾经遇到过想实时了解更多当前场景的更多内容、却发现操作较麻烦而不查询的情况吗？
5. 您本人平时使用图像处理软件来人物抠像的程度高吗？

- **调研结果**

| 调研总结 |
| ----- |
| 绝大多数受访者有使用图像处理软件的习惯 |
| 大部分受访者较感兴趣，不过有一小部分不清楚实际操作起来是否方便，保留意见 |
| 一半的受访者会，另一半则很少使用，除非特意想实现某效果 |
| 综合意见是有一部分会遇到，而更多的是在空闲的时候回忆场景时会出现想查询但麻烦的情况 |
| 大部分的受访者对人物抠像的使用度适中，还有些受访者反映抠像操作成本较高，不太经常使用 |

## ⭐️4.人工智能概率性与用户痛点

### 用户痛点：
(加值的表述是否明文且合理有实据地对映到用户痛点的表述。用户痛点参见 吴雪. 人工智能产品经理 1%*3=3%)
核心价值就是能帮助用户快速查询并实时返回图片信息，简单操作即可抠图和美颜成功，并且可对所抠的人像进行二次创作。

1. 用户缺乏一款可以一键抠图、美颜和图片风格置换结合来二次创作的软件。
2. 用户查询图片的更多信息所用时间成本较高，而因此失去了了解图片背后故事的机会。
3. 用户想对图片进行二次创意创作的操作较为复杂，让用户失去对图片创意制作的动力。
4. 用户有需要实时反馈图片更多信息的服务， 由于在碎片化阅读的时代，用户很少会花较多的精力去查询图片的更多内容。

### ⭐️5.需求列表与人工智能API加值,即**所使用的人工智能对应到其需求列表当中**

| 用户案例 | 对应的人工智能 | 重要程度 |
| ----- | ----- | ----- |
| 一个25岁的小伙想要对以前的照片进行创意制作，把自己的人像置于风景照中	| 人像分割api可以实现一键抠像和背景图片的转换结合 | 中 |
| 一个19岁的女生想给她的男朋友一个惊喜，把他们合照置于自己喜欢的马尔代夫群岛上并创意地改变图片风格	| 通过人像分割api和图像风格转换api的结合可以快速实现图片的创作与生成 | 高 |
| 一个旅游爱好者平时想对某景点、地标或展览展品的信息了解更多，却发现查找的成本较高，于是只能放弃 | 通用物体和场景识别api可以让用户得到更多的图片信息反馈 | 中 |

# 具体应用场景
1. 用户想要快速地实现一键抠像和美颜的结合
2. 用户需要快速了解图片的更多信息,可以与朋友有更多的内容进行探讨
3. 用户想要换图片风格，可以把自己抠的人像置于自己想要的背景图中，简单地实现图片转换和人像结合

# ✨二、原型

*点击进入交互体验：*

*点击进入仓库下载源文件：*

——————————————————————————————————————
### ⭐️ 1.原型1.交互及界面设计
交互及界面设计：在PRD文件中是否有说明且原型是否有做到：交互及界面设计的某个核心交互环节使用了人工智能的加值

### ⭐️ 2.原型2.信息设计5%
信息设计：在PRD文件中是否有说明且原型是否有做到：信息设计的某个核心信息或设计使用了人工智能的加值

### ⭐️ 3.原型3.原型文档5%
原型文档：多少程度上有提供MVP可交互的原型文档，供它人在Github上下载使用

# 使用者交互与设计（axure产品原型）
- 产品架构
![产品结构图](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20191225011805.png)

- 产品流程
![产品流程图](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_201912250118051.png)

## 交互及界面设计
- APP界面图
![首页](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E9%A6%96%E9%A1%B5.png)
![上传图片](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E4%B8%8A%E4%BC%A0%E5%9B%BE%E7%89%87.png)
![反馈结果](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E5%8F%8D%E9%A6%88%E7%BB%93%E6%9E%9C.png)
![抠图图片上传](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E6%8A%A0%E5%9B%BE%E5%9B%BE%E7%89%87%E4%B8%8A%E4%BC%A0.png)
![抠图成功](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E6%8A%A0%E5%9B%BE%E6%88%90%E5%8A%9F.png)
![风格置换](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E9%A3%8E%E6%A0%BC%E7%BD%AE%E6%8D%A2.png)
![选择置换风格](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E9%80%89%E6%8B%A9%E7%BD%AE%E6%8D%A2%E9%A3%8E%E6%A0%BC.png)
![置换成功](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/界面图/置换成功.png)
![分享界面](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E5%88%86%E4%BA%AB%E7%95%8C%E9%9D%A2.png)
![历史记录](https://github.com/yanzhong-su123/yanzhong-su123.github.io/blob/master/%E7%95%8C%E9%9D%A2%E5%9B%BE/%E5%8E%86%E5%8F%B2%E8%AE%B0%E5%BD%95.png)


### [原型文档下载区]()
## [原型文档交互展示]()


## （十）产品结构图
1. 产品功能结构图

2. 产品信息结构图

3. 产品流程图

4. 产品结构图

# ⭐️三、API 产品使用关键AI或机器学习之API的输出入展示
### ⭐️API1.使用水平
完整代码请点击：
实例代码
#### 1.通用物体和场景识别
##### 首先创建应用，然后获得官网中client_id 为官网获取的AK， client_secret 为官网获取的SK，来用于请求获得access_token
```
import requests 

# client_id 为官网获取的AK， client_secret 为官网获取的SK
host = 'https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials&client_id=rVkO722ZXcjRsmrL3PGmnpTm&client_secret=7eLRAaKAN0M2UnmPB0xlB5yMskN88yys'
response = requests.get(host)
if response:
    print(response.json())
```
#### 返回Access_token结果
![image.png]()
![image.png]()


#### 2.图片风格置换
```
import requests
import base64

'''
通用物体和场景识别
'''
def Picture_content_recognition():
    request_url = "https://aip.baidubce.com/rest/2.0/image-classify/v2/advanced_general"   ##申请调用百度AI的API接口的URL
    f = open('/Users/pc/Desktop/photo.jpg', 'rb')  ##打开本地图片的路径
    img = base64.b64encode(f.read())

    params = {"image":img
         }   ##设置请求参数：图片
    params["baike_num"] = str(img,'utf-8')
    access_token = '[ 24.e32e28d453badf271e6296905d123cb2.2592000.1580290786.282335-18141929]'  ##获取认证的参数值 access_token
    request_url = request_url + "?access_token=" + access_token
    headers = {'content-type': 'application/x-www-form-urlencoded'}
    response = requests.post(request_url, data=params, headers=headers)
    print (response.json())
    
if __name__ == "__main__":
    Picture_content_recognition()
```

![image.png]()
![image.png]()

#### 3.人体抠像
```
import urllib.request ##人体抠像
import urllib.error
import time

http_url = 'https://api-cn.faceplusplus.com/humanbodypp/v2/segment'  ##申请调用的API接口的URL
key = "_-mm3fWeDC8VGwrTDjCJJwX5A5qDosKi"  ##创建应用后的API_key
secret = "rKLRM6_QAwHxgMpQTMxNqoigLhgcCrqw"   ##创建应用后的API_secret
filepath = r"/Users/pc/Desktop/timg.jpg"   ##改成自己图片的路径

boundary = '----------%s' % hex(int(time.time() * 1000))
data = []
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'api_key')
data.append(key)
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'api_secret')
data.append(secret)
data.append('--%s' % boundary)
fr = open(filepath, 'rb')
data.append('Content-Disposition: form-data; name="%s"; filename=" "' % 'image_file')
data.append('Content-Type: %s\r\n' % 'application/octet-stream')
data.append(fr.read())
fr.close()
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'return_landmark')
data.append('1')
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'return_attributes')
data.append(
    "gender,age,smiling,headpose,facequality,blur,eyestatus,emotion,ethnicity,beauty,mouthstatus,eyegaze,skinstatus")
data.append('--%s--\r\n' % boundary)

for i, d in enumerate(data):
    if isinstance(d, str):
        data[i] = d.encode('utf-8')

http_body = b'\r\n'.join(data)

# build http request
req = urllib.request.Request(url=http_url, data=http_body)

# header
req.add_header('Content-Type', 'multipart/form-data; boundary=%s' % boundary)

try:
    # post data to server
    resp = urllib.request.urlopen(req, timeout=5)
    # get response
    qrcont = resp.read()
    # if you want to load as json, you should decode first,
    # for example: json.loads(qrount.decode('utf-8'))
    print(qrcont.decode('utf-8'))
except urllib.error.HTTPError as e:
    print(e.read().decode('utf-8'))
```

![image.png]()
![image.png]()


#### 4.人脸美颜
```
import urllib.request ##人脸美颜
import urllib.error
import time

http_url = 'https://api-cn.faceplusplus.com/humanbodypp/v2/segment'  ##申请调用的API接口的URL
key = "_-mm3fWeDC8VGwrTDjCJJwX5A5qDosKi"  ##创建应用后的API_key
secret = "rKLRM6_QAwHxgMpQTMxNqoigLhgcCrqw"   ##创建应用后的API_secret
filepath = r"/Users/pc/Desktop/timg.jpg"   ##改成自己图片的路径

boundary = '----------%s' % hex(int(time.time() * 1000))
data = []
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'api_key')
data.append(key)
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'api_secret')
data.append(secret)
data.append('--%s' % boundary)
fr = open(filepath, 'rb')
data.append('Content-Disposition: form-data; name="%s"; filename=" "' % 'image_file')
data.append('Content-Type: %s\r\n' % 'application/octet-stream')
data.append(fr.read())
fr.close()
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'return_landmark')
data.append('1')
data.append('--%s' % boundary)
data.append('Content-Disposition: form-data; name="%s"\r\n' % 'return_attributes')
data.append(
    "gender,age,smiling,headpose,facequality,blur,eyestatus,emotion,ethnicity,beauty,mouthstatus,eyegaze,skinstatus")
data.append('--%s--\r\n' % boundary)

for i, d in enumerate(data):
    if isinstance(d, str):
        data[i] = d.encode('utf-8')

http_body = b'\r\n'.join(data)

# build http request
req = urllib.request.Request(url=http_url, data=http_body)

# header
req.add_header('Content-Type', 'multipart/form-data; boundary=%s' % boundary)

try:
    # post data to server
    resp = urllib.request.urlopen(req, timeout=5)
    # get response
    qrcont = resp.read()
    # if you want to load as json, you should decode first,
    # for example: json.loads(qrount.decode('utf-8'))
    print(qrcont.decode('utf-8'))
except urllib.error.HTTPError as e:
    print(e.read().decode('utf-8'))
```

![image.png]()
![image.png]()


## （十一）API的运用：
1. 百度API：

```
代码示例：

```


```
代码示例：

```

## （十二）AI产品概率性：
1.	
2.	
3.	

## (十三)API使用风险评估
- AI错误率：
>> 

- 错误现象处理办法：


## 产品的可行性:


