组装中的机器人
=================

注意: 这只是个组装中的机器人，作者还在探索。

>  ``我认为，保持计算机科学的趣味举足轻重。这一学科在起步时让人乐不可支。当然，那些付钱的客户们时常会觉得被我们敷衍了。之后，我们开始信以为真。我们开始觉得，自己真的像是对成功地、无差错地、完美地使用这些机器义不容辞。我不以为然。我认为我们的责任是去拓展这一领域，将其发展到新的方向，并在私底下保持趣味。我希望计算机科学领域绝不要丧失其趣味意识。最重要的是，我希望我们不要变成传道士，不要认为你是兜售圣经的人，世界上这种人已经太多了。你所知道的有关计算的东西，其他人也都能学到。绝不要认为成功计算的钥匙只掌握在你的手里。我认为并希望，你所掌握的是智慧：那种当你第一次站在这一机器面前时就能看到它的本质的能力，这样你才能将它推向前进。''
> 
> Alan J. Perlis (生于1922年4月1日，卒于1990年2月7日）
> 从SICP摘抄


(2016.1.15): 应该算是个可靠可用的机器人了。

作者仅仅为了：

1. 自己想要一个能进行信息收发的某国内顶级IM机器人。
2. 熟悉Node的http/https request 等模块，学习HTTP基本知识。
3. 学着Promise怎么使用，如果可以Stream如何玩，这么比较好的抽象整个流程
4. 学习使用浏览器调试工具，https代理等等。甚至透明代理，iptable这种东西。。

最重要的是：

5. 好奇
6. 聊以自娱

所以，这是一堆混乱不堪的东西，希望各位老师教我做人。

## 使用须知

请为了学习和娱乐适量使用，因此造成的任何损失、影响，都由使用者自行承担，与本人无关。源代码遵循GPL v2。

当前代码使用方式

    node test.js

扫描二维码确认登录。

目前是个聊天机器人，对话引擎默认使用图灵机器人。需要自行申请图灵机器人的API，保存到`apikeys.js`文件内：

    module.exports.turingRobotApiKey = '你申请的key';

也可以在`dialog.js`里实现自己的对话系统，请参照源码。

** for fun and profit. **

## 依赖

imagemagick： 

    sudo apt-get install imagemagick

request: 

    npm install request

## TODO

- [ ] 协议文档
- [X] 分离回复逻辑
- [ ] 修复已知问题

## ChangLog

### 2016.1.14

- 实现登录长连接 #8
- 分离替换api

### 2016.1.13

- 重新实现长连接，修复多条消息会重新出现的问题 #5
- 分离回复逻辑 #2
- 捕获服务器断开消息自动退出 #1

### 2016.1.12

- 修复遗漏消息的问题
- 接入图灵机器人实现聊天机器人
- 清理代码
- 完成用request替换所有原生模块

### 2016.1.11

- 完成基本的回复机器人功能。
