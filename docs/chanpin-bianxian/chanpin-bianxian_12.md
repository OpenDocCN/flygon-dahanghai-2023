
# (精华帖)(110 赞)程序员的视角看问题：想把视频转成文字，用代码来解决，最终实现问题的解决 + 收益

作者：  佳恺

日期：2022-10-24

大家好，我是佳恺，微信昵称北极，是一名爱折腾的野生程序员。

因为我平时会报一些网课，在学习视频课程的过程中，需要做笔记，方便复习。但是边看视频边记笔记，遇到讲的快的地方，速度跟不上，反复拉进度条回看，很麻烦，效率也低，我就会想有没有可以直接把视频转成文字的工具呢？

今天跟大家分享我是如何通过制作一款小工具实现视频转文字自动化，解决了自己的需求，之后验证他人的需求存在，完成推广变现的过程。

 

 

这个项目现在的情况是，小程序累计用户 12w，日 IP 1.5k 左右，2 个公众号粉丝 2.7w，微信好友 2k。（数据截图我在文末附上）

变现的话，确实比较少，1 个月只有 4-5k。不过这个项目算是完成了从需求-产品-流量再到变现的一个全过程，希望对新手同学有帮助。

文章内容大概分为三个部分进行：

第一个部分讲的是从我遇到的一个问题发现的小机会，这部分想说明我们可以多从平时所遇到的问题去发现机会挖掘需求，因为是自己亲身经历过的，更深刻，也更能从用户角度去思考，做成的信心也越大。

第二个部分分成 4 个小节，第 1 小节是需求调研，我在这部分介绍怎么通过百度指数，去验证别人是不是也有这个需求，只有验证需求后，我们才能判断这个需求有多大，竞争有多大，值不值得我们花时间和精力去做这个项目。

第 2 小节，工具开发这部分没有讲技术、代码上的东西，主要是想说做项目最好是快速建立 mvp，然后优化迭代，这样才能快速上线获得反馈。

第 3 小节，运营推广这部分主要介绍我通过微信公众号 seo 获取流量的过程，我认为微信公众号 seo 截流是也一种快速获取稳定被动流量的方式，而且从我的推广过程来看，比百度 seo 要简单不少，重点就是取一个包含关键词的公众号名称。

第 4 小节，迭代变现这部分介绍我根据用户反馈优化工具，从这些反馈中挖掘更深层次的需求来变现的过程，其实只要解决了用户的问题，变现只是顺带的事儿。

 

 

第三个部分，是我在这个项目中的几点思考分享。

一、从自己遇到的问题发现需求

可能生财有术的圈友对商业、产品、项目、副业都比较感兴趣，了解的需求挖掘方法都比较多，之前很多高手也分享过：

https://shengcaiyoushu01.feishu.cn/docs/doccnBEA2JShVYfOzBuhiu6Rdxe#joU9zQ  然后，我自己做过一些项目，也用过一些挖掘方法，但是大部分还是从自己遇到的问题或者感兴趣领域来挖掘需求。特别是自己遇到的问题，解决这个问题的方法、经验、产品，很可能也是别人遇到这问题所需要的。

这个视频转文字工具的由来，是因为我平时会报一些网课，在学习视频课程的过程中，需要做笔记，方便复习。

之前是边看视频边记笔记，遇到讲的快的地方，速度跟不上，就只有反复拉进度条回看，这种记笔记的方式效率很低。多两次后，就感觉太麻烦了，我就想，有没有可以直接把视频转成文字的工具呢。

然后去百度搜索，发现百度首页除了广告好像还没有能直接转视频的工具，有的是介绍怎么用 ffmpeg 然后结合调用百度接口转换，另外是有开发者做的一款小程序，在知乎里推广。

 

 

不过这两种，前者对于普通用户来说，命令行操作很麻烦，而且很多人看到电脑黑框就怕。小程序也不太适合转网课这种大文件做笔记。

我隐隐感觉这是个小机会，可以做成小工具，既能解决自己的问题，说不定还能帮助到其他人，顺便卖出去赚点儿小钱。

二、项目全过程

**1. **需求调研，通过百度指数，验证需求是否存在

当然，如果只是解决自己的问题，直接干就是。因为我已经有了做工具的念头，所以还有一步是必要的，验证别人是不是也有这个需求。

平时我验证需求主要还是查各大平台的指数，百度指数、微信指数，5118 之类的。因为如果关键词有指数，说明极大概率别人也在搜索这个词。

当时去百度指数查询了“视频转文字”这个关键词。写这个分享的时候我查了下，这个词显示未收录。不过当时这个词的指数在 200~300 这样，说明其他人对视频转文字也有需求，而且指数比较低，竞争肯定相对语音识别小很多，推广起来要容易些。

关于指数的查看方法，先进入百度指数官网 index.baidu.com，在输入框里输入想要查询的关键词，点开始探索，我当时查的是“视频转文字”，现在没了，我们随便输入一个“小罐茶”，可以发现平均有 1000 的指数。

 

 

但是我们怎么去判断这个词需求到底大不大呢，这时我们可以输入一个熟悉的一看用户就很多的词，比如“王者荣耀”，这个词指数是 5w 多，这样对比能大概看出自己关键词在什么量级上。

![](img/chanpin-bianxian_0350.png)

其实除了用百度指数查，我更推荐 5118 这样的关键词分析工具，它的数据比较全面，使用方法类似，我用 5118 查出来的“视频转文字”的数据。

 

 

![](img/chanpin-bianxian_0355.png)

**2. **工具开发，先完成，再优化

确定好需求后就是工具的开发，然后我个人的理解是，作为个人或者小团队在最初开发产品的时候，最好是把精力集中在满足用户最核心需求上，先完成，跑通流程，再优化。

就像这个视频转文字工具，虽然前后开发了三个版本：电脑版、小程序版、网页版，中间经历了很多次升级优化。

但是最初，我只写了一个很粗糙的电脑版，推广出去，有了用户之后，再根据用户提出的问题和建议，优化迭代出小程序和网页版。

 

 

![](img/chanpin-bianxian_0360.png)

**3. **推广运营，我采用的被动获取流量的方式

工具完成后，接下来就是怎么推广了，推广方式很多，我还是更喜欢 seo。

我理解的 seo 不只是百度或者 google，只要是通过搜索引擎获取流量应该都算是 seo，比如抖音、知乎、微信、b 站都有搜索功能，有搜索的地方就可以 seo，对吧。

**① **通过**seo**获取被动流量

因为不太喜欢到处发广告，希望最好是用户有这个需求，然后通过搜索找过来这样，也不会打扰到不需要的人。所以选择了 seo 被动获取流量。

我开始用 wordpress 搭了个博客，设置好网站标题，写了几篇标题和内容包含“视频转文字”、“视频转文字工具”介绍软件和使用方法的文章。

 

 

不过百度 seo 周期很长，一会儿也看不到效果，所以就在想有没有其他的推广方式。刚好那段时间在生财有术看到了公众号 seo 截流的文章，也是可以获取被动流量的，就按照文章里面的内容操作起来了。

先在微信指数上面查看“视频转文字”的指数，发现没收录（现在有了）。但是，我想，百度有人搜索，微信这么大的用户量，也一定有人搜（还好当时百度有百度指数），可能是没人提交，管他的，先试一试。

我把公众号名称设置成“视频转文字工具”，然后把简介设置成视频转文字、视频转文字软件之类的，菜单也设置成关键词，又写了几篇标题包含这些关键词的文章介绍工具使用方法。

公众号 seo 起效果比百度快太多了，没过几天，就开始有关注了，刚开始每天只有几个，然后涨到 10 来个。

前面说到想卖给其他人赚点儿小钱，这时我在生财有术看到包括亦仁大大在内的好几个大佬都提到利他、长期主义这两个词，深受启发。

想到接口费用一年也用不到多少钱，决定干脆就直接免费，赚个人气，人气起来了，后面应该有变现的机会，不着急。

所以在简介和文章上都用上“免费”的字样。慢慢的公众号排到了首页，每天稳定有 40、50 个关注。

 

 

![](img/chanpin-bianxian_0369.png)

 

 

![](img/chanpin-bianxian_0374.png)

 

 

![](img/chanpin-bianxian_0379.png)

 

 

![](img/chanpin-bianxian_0384.png)

 

 

![](img/chanpin-bianxian_0389.png)

 

 

![](img/chanpin-bianxian_0394.png)

 

 

![](img/chanpin-bianxian_0399.png)

 

 

![](img/chanpin-bianxian_0404.png)

这个量，持续了很久，直到公众号差不多有 1.3w 粉丝，突然某一天粉丝没有新增了。查看排名发现微信调整排名规则，把服务搜索和认证公众号排到前面去了。

没办法，只有换个服务号，申请服务搜索，重新操作了一遍，到现在，新号 1.4w 粉丝，每天有 150 左右的新增关注。

**② **软件留的小尾巴

另外块流量倒是让我挺惊喜的，就是开发电脑版的时候，为了方便后续进群更新，在软件上留了微信号，说可以加微信进群获取更新。

加微信的用户居然有 2000 了。这些好友，有少部分是公众号下载软件后加来的，还有部分是有的博主分享后加来的，还有一部分是有人拿这个工具去卖钱，购买软件的用户加过来找售后，这确实是我万万没想到的。

**4. **迭代及变现：围绕用户需求优化迭代

一款软件、一个项目，不可能一上来就非常完善，或多或少都会经历版本迭代和优化，慢慢让流程更标准，用户体验更好，这款很简单的工具也不例外。

 

 

比如语音识别准确率低的问题，刚开始用某厂的语音识别接口，有不少人提出准确率好像比较低的问题，开始我就觉得是因为发音不够标准，声音不够清晰导致的识别率低。

后来我对比了几家云服务商发现，同样的一段录音结果，识别率确实是不一样的，自己对比下来是腾讯的稍微好一点儿，所以把接口换成了腾讯的。

后来又有用户提出，电脑版虽然转文字性能更好，但是需要下载，换一台电脑又得重新下，不能随时随地使用，不是很方便。

确实，看起来还是网页和小程序方便一些。特别是小程序，只要有微信就能用，现在谁手机里没个微信呢？使用和传播都很方便。然后我又花了一周时间，开发了网页版（免费网页版因为用的人少后来被废弃了）和小程序。

小程序和网页版上线后，在公众号做好跳转链接。小程序用的和公众号一样的套路，使用包含“视频转文字”关键词的名称和简介，配合服务搜索，流量也慢慢积累起来了。

 

 

![](img/chanpin-bianxian_0413.png)

 

 

![](img/chanpin-bianxian_0418.png)

 

 

![](img/chanpin-bianxian_0423.png)

 

 

![](img/chanpin-bianxian_0428.png)

随着流量稳定，也没什么事干，就想着能不能在此基础上做一些变现。开始选择挂微信广告，结果每天只有几毛钱，放弃。

然后就想能不能用在生财有术被提过多次三级火箭的理论做变现。免费用户里，确实还有没被满足的需求，比如其他语种或者方言，需要说话标注时间等等。

根据这些需求我模仿着前文提到在知乎里做推广的那个小程序开发了付费功能。刚上线付费功能也没什么人用，我想的是等他慢慢积累，虽然转化率低，用户基数大了，付费用户就多了。

慢慢的小程序也有了付费用户，然后又有更多的优化建议提出来，比如 1gb 以上的大文件小程序比较吃力，需要批量上传，大文件需要断点续传，需要区分人说话等等，我又对之前的免费版进行改造做成了现在的付费网页版。

经过 10 多个版本的迭代，用户在使用中经常碰到的问题，我都一一进行了优化，目前小程序和网页版都比较稳定了，也有一点稳定的被动收入了。

目前收入有三个部分，小程序充值 1k 出头，网页版扫码支付 500，另外就是直接找我买卡密的大概一个月有 3k。

 

 

![](img/chanpin-bianxian_0433.png)

 

 

![](img/chanpin-bianxian_0438.png)

 

 

![](img/chanpin-bianxian_0443.png)

 

 

![](img/chanpin-bianxian_0448.png)

 

 

![](img/chanpin-bianxian_0453.png)

三、我在这个项目中的几点思考

以上就是这个视频转文字工具从需求-产品-流量再到变现的一个完整过程了。最后再说说，我在这个过程中的几点思考。

第一个是做产品或者项目，如果从满足需求和解决问题出发来构建，做成的概率会更大一些的，并且验证需求最好是落实到数据上。

第二个是做项目可以从细分需求切入，这样用户量可能少一些，但是竞争小运营推广更容易，可以等细分做起来之后，再回头覆盖大的需求也不迟。

第三个是我感觉是微信 seo 见效很快，做项目的同学真的可以尝试一下。

最后一个是关于编程和 ai，编程和 ai 确实是很好的杠杆，它们能代替我们做一些重复繁琐的工作，提高效率的同时解放我们的双手。

懂技术的同学可以很好的利用它们，解决问题，实现流程自动化，降低边际成本，打造被动收入。那不懂技术的同学呢?这不有懂技术的同学嘛。

 

 

最后的最后，附上这个项目的数据情况截图，供有需要的同学参考，我们一起“生财有术”！

 

 

![](img/chanpin-bianxian_0462.png)

 

 

![](img/chanpin-bianxian_0467.png)

 

 

![](img/chanpin-bianxian_0472.png)

 

 

![](img/chanpin-bianxian_0477.png)

 

 

![](img/chanpin-bianxian_0482.png)

 

 

![](img/chanpin-bianxian_0487.png)

 

 

![](img/chanpin-bianxian_0492.png)

 

 

![](img/chanpin-bianxian_0497.png)

 

 

![](img/chanpin-bianxian_0502.png)

 

 

![](img/chanpin-bianxian_0507.png)

 

 

![](img/chanpin-bianxian_0512.png)

 

 

![](img/chanpin-bianxian_0517.png)

评论区：

Fus : 请问小程序收款是直接到企业公户，那这一块还得跟税务有关系，有其它解决方案不？

佳恺 : 我自己是对公的哈，你看下 xorpay 之类的，能解决你的问题不  Fus : 那个就是微信小微支付，到个人卡的，费率比较高，市场服务商要收 2% 码叔编程 : 小微商户默认是 0.38%，找服务商申请还可以更低

iMairy : 我也是类似的业务模式，目前采用的是企业微信收款到个人帐户，手动后台给用户升级

vice : 大佬厉害，网页扫码支付，卡密是有三方的可以用吗，还是都是自己写的啊  阿虎 : 完整项目操作流程，可复制，精华文

佳恺 : 卡密没走第三方哈，主要是方便量大的用户和代理定制使用