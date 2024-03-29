# self-management-group
 基于QQ群的他律与自我管理结合的系统，使用自然语言编写

# 项目简介

这个项目本质上是一套规则，可以应用于一个QQ群，利用了现有的QQ群的各种功能（群相册，群文件等）来实现自我管理。

说是自我管理，但毕竟是个群，也借用了群内其他成员无形中形成的监督环境来监督你完成目标。

**将本项目上传的目的是供有意愿建立类似群聊的人借鉴规则。**

现在有一个于2019年4月26日创建的实验群正在运用这一套规则，下文提到的一些例子都是出自实验群。

# 规则简介

- **[打卡系统](#打卡系统)：** 本群的打卡系统利用了QQ群的群相册。如果你有想要打卡的项目，可以在登记了信息之后创建群相册用于打卡，由管理员以及全体群成员监督，**超过一定天数未打卡（比如连续三天未打卡），就会删除对应的相册，并扣除一定的积分**。而达到一定天数可以将相册归档，获得与持续天数正相关的积分。
- **[反思系统](#反思系统)：** 作为本群成员，需要每周周日总结一下本周的收获，并以文字的形式发到群内。如果没有收获，也需要在群里说明（例如说：“本周无总结”）。**没有声明本周没有总结且未总结的**，扣除一定的积分，在下一周周日结算之前补回，则取消扣分。正常总结会获得一定量的积分。
- **积分系统：** 进群之后初始积分为0，若**积分为负数且在下一周周日结算之前仍然为负数**，则会强制离开群聊。
- **邀请系统：** 本群采用邀请制，每个月最多邀请一个愿意遵守群规则的人入群。如果没有这样的人选，这个月就不邀请，宁缺毋滥。
- **文件系统：** 为了方便学习交流，如果需要上传文件，请将文件上传到对应的文件夹，并使得看文件名就知道这个文件的作用，多版本文件请用6位数日期+修改次数的后缀
- **反馈系统：** 可在本项目的issue中提出对群规则的修改建议。对于实验群的群成员，如果没有github账号，可以向管理员提出修改建议
- **群活动：** 群内会不定期地进行一些活动，自愿参与。



简单来说，想要留在这个群里面，最简单的方式是只需要在每周日发一条“本周无总结”，维持积分不为负。

而在这个基础上，你可以选择群里面提供的规则来进行自我提升、自我管理，也可以向管理员提出自己的规则提案、活动提案。

**本群提供的是一种氛围，一种监督环境，至于能否从中获得提升，还需要看你自己。**



详细内容见下：

## 打卡系统

由一个.xlsx文件（即电子表格文件）来实现。下图为示意图。

![](https://raw.githubusercontent.com/HaneChiri/PicBed/master/blog_images/20190818105321.png)

### 打卡定义

在此处，“打卡”的定义是：在自己的打卡相册内上传图片（截图，照片等），无关图片内容（别太偏题就行）

未达成“打卡相册登记表”内的打卡目标判断标准也没有关系，**群规则仅仅监督你有没有做，而不关心你做得好不好**（不然管理员要累死了）。比如你今天很累，完成不了今天背单词50个的目标，你可以只背十几个甚至一两个就截图上传。

重点是你是否去做，而不是做得好不好，**打卡系统是为了创建并保持你的习惯触发动作**

### 作用

帮助养成习惯

### 创建打卡相册

创建打卡相册需要以下步骤：

1. 在群文件内下载“打卡相册登记表xxxxxx-x.xlsx”文件
2. 在其中根据工作表“打卡相册字段描述”内的说明，在工作表“打卡相册登记表”内填写好对应的信息
3. 将文件名修改为“打卡相册登记表+6位数日期+任意分隔符+这一天第几次修改”，
   如：“打卡相册登记表190617_1“代表2019年6月17日的第一次修改。并将文件上传
4. 在群相册创建自己的打卡相册，开始打卡

### 打卡相册规则

下面只列出比较重要的几个规则，具体的积分计算规则见[这里](https://hanechiri.github.io/post/excel_clock_in_album/)

- 相册状态：正在进行、放弃、失败、归档
- 如果**连续三天**未打卡，管理员就删除相册，并在登记表内将相册状态设置为“失败”。
- **不创建打卡不扣分，创建打卡而未坚持下来会扣分。没有请假制度，创建打卡前请考虑好**
- 对于有期限的相册，比如打卡目标是“两周读完《xxx》”，那么在结束日期时，可以将其状态设置为“归档”。相册资源回收（删除或改作他用），避免资源闲置。若**持续时间大于等于一百天**，则可以选择保留相册。（可以给其他群员作榜样）
- 对于没有期限的相册，比如“每天背单词”，那么在**创建时间满三十天**后就可以选择“归档”（三十天应该够养成一个小习惯了），删除规则同上一条。
- 相册删除后，相册记录还会保留在登记表里面，是**公开的**哦。



## 反思系统

其登记表与打卡相册登记表使用同一个工作簿，积分计算规则见[这里](https://hanechiri.github.io/post/excel_weekly_sign)

![](https://raw.githubusercontent.com/HaneChiri/PicBed/master/blog_images/20190818111657.png)

### 作用

1. 在群文件内回顾与反思自己这一周做了什么
2. 为你自己的进一步总结留下材料（比如哪天想来个年总结或者月总结的时候）
3. 看到别人学习了自己却没有而产生激励效果
4. 保持群内一定的活跃度，去除不活跃成员
5. 作为群内一个基本的群活动，强化学习氛围

### 规则

- 每周日，每个人在群聊天发一个周总结，内容是自己这周学习了什么，没有限制，只是给大家一个自我反省的机会。
- 如果没有可以写的东西，那么也在群里面报备，方式为在群聊天中说：“本周无总结”或者别的能表明这一事实的话。别有压力，只是回复一句话的功夫。
- 无论总结多少，只要总结了，都会获得一定量的积分。
- 如果周日那一天状态不好或者很忙，可以在群里@管理员，告知推迟时间（不可超过下周周日），只要在报备的时间之前补了总结，也可以获得总结积分。
- 如果没有报备也没有在截止之前发周总结，可以在下一周总结之前补。如果没有补，则会扣除一定的积分。
- 每周所有成员的周总结将会被管理员整理到一个文件中，发到群内，即**周总结是公开的**，方便你随时查看自己的周总结以及自己下周的目标。
- 尽量使用markdown语法，方便管理员整理。如果你不了解什么是markdown，那么就只需要在你的总结前面加上一行“## 你的昵称”即可。如果你想要学习markdown，可以参考我在b站发的[这个视频](https://www.bilibili.com/video/av56611630/)。本篇文章就是使用markdown语法来书写的。

### 总结示例

内容没有限制，想写什么都可以，不限字数，但是最起码的格式是，在总结前面加上“## 你的昵称”

以下内容仅供参考，可以根据自己的喜好来增加或删除模块。

#### 简易总结示例

```markdown
## 憧憬少

本周没做什么事情
```

#### 详细总结示例

摘自实验群“周总结week5”，使用了markdown语法，可以在群文件的“周报”文件夹中找到它，看一下markdown的渲染效果。

```markdown
## 憧憬少

### 本周做了什么

- 驾校练完了右侧倒车入库，开始学习左侧
- （周一）完成信息门户密码加密模块并上传github和[编写博客](https://hanechiri.github.io/post/portal_login_encrypt/#more)
- （周三）完成信息门户模拟登录模块并上传[github](https://github.com/HaneChiri/CHD_portal_login)和[编写博客](https://hanechiri.github.io/post/portal_login/#more)
- 驾校排队练车的时候无聊，开始使用墨者写作APP来重新开始以前放弃的小说并在群里连载
- （周六）写了一个python脚本用于自动启动明日方舟的代理指挥，学习了`pyautogui`库。
- （周日）发布上述脚本的[介绍视频](https://www.bilibili.com/video/av60038926/)以及上传脚本和打包的exe到[github](https://github.com/HaneChiri/arknights_assist)

### 本周的目标有没有达到

【目标链编号，每完成一个目标，生成下一个目标，编号增加，未完成则归零】

- [x] 【1】一周四次运动
- [x] 【0】一周三次，每天写代码半小时

### 下周的目标

- [ ] 【2】一周四次运动，包括不限于跑步，散步等
- [ ] 【1】一周三次，每天写代码半小时
- [ ] 【0】每天利用time meter记录时间开销

### 概括这一周

分数：85%

- 在驾校遇到了同一个高中的同学（虽然不是一个班不认识）
- 做了挺多事情
```

## 群活动

可以在群内向管理员提出群活动的建议。

关于群活动的一些例子：

### #1学期总结

【活动】学期总结

【编号】#1（也就是第一次活动）

【时间】2019-6-21~2019-7-10

【内容】本学期已经告一段落，学科的内容是否考完试就忘得差不多了呢？为了避免这一学期白学，各位学研都市居民可以在活动时间内在群文件的群活动作品提交文件夹内提交自己的学期总结。
形式不限，可以是手写总结拍照，可以是知识框架思维导图，可以是笔记文件，可以是录音讲解等。

【存档】活动结束之后，会将群文件中提交的总结统一打包，保存到群活动文件夹中，群活动提交文件夹会被清空。

【排名】活动结束之后，会进行作品投票，票数最多的参与者可以获得奖励

【奖励】目前我能想到的奖励就只有30天自定义专属头衔了（此时还没有创建积分系统）

### #2暑假总结

【活动】暑假总结 

【编号】#2 

【时间】2019-8-19~2019-8-25 

【内容】暑假只剩下最后一周了，这个暑假做了些什么有意义的事情呢？暑假开始时定的目标达到了吗？对新的学期有什么规划吗？无论总结地好与不好，都可以试着回顾一下。 

【参与】提交PDF格式的文件。提交即视为参与 

【存档】活动结束之后，会将群文件中提交的总结统一打包，保存到群活动文件夹中，群活动提交文件夹会被清空。 

【奖励】活动结束之后，会进行作品投票。第一名获得8积分，第二名4积分，第三名2积分





# 管理员周常

管理员在每周结算日需要做的事情：

- 清空群内临时文件夹以及回收站文件夹内的文件
- 整理本周周总结为文件形式，上传到群内
- 下载登记表
- 在登记表内登记发布周总结的成员，并在群内提醒未发布的成员
- 登记补交上周周总结的成员
- 处理超时未打卡的相册
- 将修改后的登记表修改日期版本号，上传到群内
