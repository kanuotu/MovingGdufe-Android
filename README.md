# 移动广财 App
源于毕设，基于开源。产品截图见 [官网](http://www.wintercoder.com:8080/)

App对接了广财的教务、信息门户、一卡通、图书馆等系统，包含 Dr.com 功能，数据均为爬取获取，无学校官方接口。  
这个项目是客户端源码，服务端代码不开源，但开放Api接口。

![](readme/function.png)
功能如图，图中蓝色部分为入口较深的功能，启动通知为打开App时，服务端发送的通知；生日祝福是在公历生日当日打开App有弹窗祝福。

如需导入项目但不熟安卓，转见 [客户端-安装指南.md](%E5%AE%A2%E6%88%B7%E7%AB%AF-%E5%AE%89%E8%A3%85%E6%8C%87%E5%8D%97.md)

## API接口
将 [该地址](http://www.wintercoder.com:8080/apidoc) 的 `localhost` 换成 `api.wintercoder.com`。  
另外建议长期使用Api接口的联系下管理员，因未来会修改接口的身份、安全验证，方便到时通知。

## 广告
1. 长期招聘维护 移动广财 的技术人员。
1. 如有针对广财的产品，打算发布到该 [WeGdufe](https://github.com/WeGdufe/) organization，可在 [organization页](https://github.com/WeGdufe) 点右侧头像发email给组织成员，目前找 [wintercoder](https://github.com/wintercoder) 即可。


## 技术说明
技术框架： Rxjava 2.0.1、Retrofit 2.1.0、Litepal 1.4.1 [框架学习教程戳这](学习教程.txt)

	逻辑根目录/
    ├─activity          活动页面
    ├─adapter           数据和列表的中介-适配器
    ├─api               与服务端的接口交接部分
    ├─fragment          Tab页面碎片
    ├─model             服务端返回的数据封装实体
    ├─util              工具包
    │  └─drcom              城市热点模块
    │  └─widget             桌面小部件相关
    └─widget            自定义控件，如课表页、可缩放的ImageView
    页面视图根目录/
    ├─drawable          颜色/样式选择器
    │  └─sehedule           课表页面的颜色形状表
    ├─layout            布局文件
    ├─menu              标题栏的按钮页面
    ├─mipmap-hdpi       针对不同手机分辨率的图片资源，下同
    ├─mipmap-mdpi
    ├─mipmap-xhdpi
    ├─mipmap-xxhdpi
    ├─mipmap-xxxhdpi
    └─values            字符串、颜色等常量


## 贡献代码
贡献流程：Fork该项目 -> 修改好代码后Push到你的项目 -> 在该项目发起Pull request。  如果想加入团队长期维护，发邮件至 `movinggdufe@163.com` 或者通过Q群 `631036490` 等其他渠道联系项目管理员。  

近期客户端功能需求：  
1. 按课表空白处，可手动增加课表，方便双学位童鞋。对于已有课程单击可编辑。  
1. 英汉翻译。  
1. 美化登陆界面、排课表、校历、地图、常用电话等界面。  
1. 登陆页面增加个文本提示提供给 已毕业学生和非本校学生，点击即可以测试账号登陆。  
1. iPhone端。  

其他需要与服务器沟通的需求：  
1. **更换域名和端口**，同时征集产品新域名。  
1. API接口密码字段加密，增加Apikey字段，限制可用的客户端。  
1. 教师端。  
1. 图书馆Top100热门书。  

长远需求：  
1. 校园外卖，配送可由商家配送。  
1. 实名社交聊天区，必须实名，如需匿名则提示用户后台可见实名信息，提供校区选择功能。  
1. 与老师的IM交流：我校分校区真是坑，在引入老师、学校管理员角色后增加校园咨询功能，让学生和老师能够进行线上沟通，学生也可以选择发短信给老师（经过服务器发送，不在客户端显示老师号码），短信价格由学生支付。老师可以选择单发和群发短信给指定班级的同学做通知，通知可为App、公众号、短信推送。  
1. 讲座、社团活动信息，增加信息个性化推送、活动信息关注功能，如给缺少创新创业素质拓展分的学生主动推送创新创业类活动。  

## For 其他学校
各系统情况：  
- 教务系统： 湖南强智科技 http://jwxt.gdufe.edu.cn/jsxsd/    
- 图书系统：   江苏汇文 http://opac.library.gdufe.edu.cn/opac/search.php  
- 信息门户： 江苏金智教育 http://my.gdufe.edu.cn/  

对于Dr.com哆点登陆可见该分离后的项目：https://github.com/wintercoder/Gdufe-Drcom-Android

## License
[GPL V3](LICENSE)  
若你用该软件或者API接口开发了其他产品且发布使用，那么你也需要开源你的产品。  
未经允许，不得使用移动广财或本软件贡献者名称为你的产品做宣传、推广等。 