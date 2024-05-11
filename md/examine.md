# 机器人审核规则解读

### 一、 机器人提审流程
机器人上线前需要完成平台审核，因此开发者须将机器人的语料配置、功能配置和自测报告提交平台审核，如果审核不通过机器人将无法上线，可以优化后进行二次提审
###### 1.1注册-上架流程
<div align=center><img src="./img/shangjia.png" /></div>

###### 1.2 提审-商家详细流程
<div align=center><img src="./img/shangjiaxiangxi.png"/></div>

### 二、机器人提审时效

当日17：00前提审的机器人，当日审核完毕  
当日17：00后提审的机器人，次日审核完毕  
请勿频繁催审，若有紧急情况请联系产品值班小助理~  
可在自测报告中留下你在 QQ开发者社区-频道昵称 ，若审核出现特殊问题会在频道内与你进行联系，

### 三、机器人审核标准

##### 1.遵守“平台运营规范”
网址链接：[](https://bot.q.qq.com/wiki/business/),此规范可以从一定程度上帮您解决开发/运营/提审QQ频道机器人过程中遇到的疑问~
PS：一切违反运营规范的行为都无法通过机器人审核，以及导致机器人下架、封禁、主体封禁等处罚，请各位开发者务必遵守机器人运营规范，避免造成不必要损失。

##### 2.资料卡、功能指令基本审核规则



| 问题类型 | 详细内容参考 |  
| ---- | ----|
| 资料卡问题 | 机器人名字不足4个字 |  
|  | 素材模糊 |  
|  | 【资料卡使用素材/资料卡描述】与机器人无关 |  
|  | 涉黄赌毒政、诈骗、黑产、暴力、血腥、低俗等服务、内容描述，存在与腾讯平台对抗行为，一律不通过 |  
|  | 存在自行广告招商内容 |  
|  | 存在联系信息 |  
|  | 冒用腾讯官方、机器人内容使用腾讯官方素材 |  
| 功能违规 | 涉黄赌毒政、诈骗、黑产、暴力、血腥、低俗等服务、内容描述，存在与腾讯平台对抗行为，一律不通过 |  
|  | 涉及欺诈、赌博、竞猜、抽奖等违规内容或行为 |  
|  | 设计过度营销、卡达营销问题 |  
|  | 未经备案与报备随意跳出QQ外站行为 |  
|  | 未经用户收钱获取用户信息行为 |  
|  | 引导用户在其他平台进行充值的行为，除已备案过的赞助网站 |  
|  | 冒用腾讯官方，机器人内容使用了腾讯官方素材 |  
|  | 无资质、且涉及新闻资讯类功能 |  
|  | 涉及明星八卦、资讯、动态、行程、互动、粉丝、榜单、打榜、应援、追星、影视排行等相关功能及文案 |  
|  | 内容涉及不宜未成年接触的内容或服务，占卜、迷信等 |  
|  | 多次提交相同机器人行为 |  
| 功能配置 | 机器人指令过于简单且不够完善，仅有1-3个基础指令，且实际使用中功能描述不清楚 |  
|  | 指令无响应 |  
|  | 指令回复与自测报告描述不用 |  
|  | 实测功能未在自测报告中说明 |  
|  | 实际功能少于自测报告中提供的功能 |  
|  | 特殊指令操作方法未在自测报告中说明 |  
|  | 自测报告未按标准格式编辑 |  

##### 3.自测报告标准
[机器人自测报告模板-2021](
https://docs.qq.com/sheet/DS1VtV3hBTXV5TEFK)

3.1 注意事项  
- 务必提前进行指今自测，确保指令有呈现在机器人指令列表中，唤起正常，以及回复内容正确  
- 清晰表述每一个提审的指令如何使用，可以在备注处附上示例;  
- 认真核对自测报告指令与文际提审指令数量，描述是否完全相同，避免出现实测功能未自测报告中说明情况;  
- 若指今需要 特殊操作权限、操作流程等，务必在白测报告中说明  
- 若指令需要到固定频道体验，请提供有权限的账号、跳转频道的操作权限、准确频道号名称、以及- 适当的流程图示例，避免审核人员加入频道值要等待审枇通过后再进行指令测试，造成审核慢，测试不准确情况;  
- 若指令涉及拥定游戏账号，请提供响应的游戏账号，以及适当的操作流程图不例  
- 可以在自测报告中加入自己在Q0开发者社区的 频道昵称，若机器人测试有任何问题，审核人员可以第一时间联系到你，快速解决问题。

3.2 自测报告示例  
<div align=center><img src="./img/zice.png"/></div>  

### 四、机器人审核拒绝常见问题解析、优化指引

##### 1、为什么出现“指令无响应”?  

- 提审时未将沙箱域名切换回正式域名  
- 指令有特殊条件，但自测报告中未说明，指令进管理员可用  
- 指令存在特殊情况，但逻辑并没有覆盖，例“该指令每目只可用一次"等  
- 指令在代码中未做/空格兼容适配  
- 提审期间机器人未在线  
- 机器人所需特殊权限，未在自测报告中说明  
- 功能涉及需绑定第三方平台账号，未再白测报告中附上测试账号与密码，导致审核人员无法测试  

##### 2、功能配置描述与实际功能不符是怎么回事?  

指定回复内容与自测报告描述不同  
实测力能未在白测报告中说明  
实际功能少于自测报告中提供的功能  
具体体现为：  
    - 功能指令——输入功能指令 A，除返回开发者自测报告显示的指定内容外，另跳出多条无
关内容  
    - 功能播令—输入功能指令 A，开发者自测报告指定返回内容 B，但实际返回内容为C  
    - 功能配置实测功能数大于开发者提供的功能配置描述  
    - 功能配置—，实测功能数小于开发者提供的功能配置描述  
    - 功能配置——功能描述为A类型，实测功能为B关型  

##### 3、为什么我的白测报告被审核拒绝?  

- 自测限告未提供功能异明，仅上传平着水的内容  
- 测式人员体验到自测报告来详细说明的功能被直接打回  
- 自测报告信息模极不清，如每天上午推送消息，未提供具体推送时间

##### 4、提审后，反馈“机器人名称违局平台规则”需如何改进?  

- 名字长须必须大于4个字，不得与其他机器人名字重复  
- 名字需能休现机器人功能、特色或者IP相关，
- 用个人名字或昵称，以及过于宽泛的词语  
- 特殊符号、火星文、无意义字母文字堆砌
- 违规或包含营销类词语  
- 冒用腾讯言方，机器人内容使用了腾讯官方素材  
- 存在联系信息  
- 存在自行广告招商内容  

### 五、审核问题反馈  

##### 1. 日常反馈  

若日常提审机器人有疑问/对于机器人提审结果存在疑问，可以到 QQ 开发者社区。【审核及
bug】子频道发帖反馈，会有小助理定期协助您解决。  
帖子必备信息如下  
- bot id  
- 提审时间  
- 涉及问题  
- 问题详细描述  
- 附上相关截图  

##### 2.建议反馈  

点击链接：[其他常见问题，建议反馈](https://wj.qq.com/s2/11202512/28b6/)，进行反馈吧，小助理会定期进行反馈回收，不断优化机器人审核相关事宜，协助大家解决更多机器人提审相关问题!