
# (30 赞)Chrome PDF 插件从 0 到 1 的试错经验与踩坑复盘

作者：  颜过

日期：2021-08-11

Chrome 插件从 0 到 1 的试错经验

PS：之前这篇所有内容只在内部小圈子分享过，最近一次分享在帅张张哥的群里。之前了解我的财友，最大的标签是跨境电商，但今天不聊跨境，聊聊试错出海小工具。

作为程序员的朋友，可能大家关注点基本都在技术精进上，其它可能很少关注，今天的分享内容主要是围绕着技术之外的一些东西分享，不足之处，后面应该还会有迭代的，到时候再跟大家来分享。

一，选哪个主战场

主战场，主要还是先从开发难度还有开发时间两个维度来说的。

给个参考排序：电脑 PC 端>=手机端 Apps>Web 端 SAAS 或网站>插件（电商类 Apps，例如 Shopify Apps，Chrome 插件，wordpress+WooCommerce 等周边插件<即 wp+woo>）。

因为过往的跨境电商经验，优选电商类小工具，那就是 shopify apps 或 wp+woo，但前者上架其实难度大很多，后者相对成熟一些，需要也多，例如很多 shopify apps 的需求都可以直接搬运到 wp+woo 上来实现。但时间卡在那里，另外还有一个点，就是快速反馈原则，即快速从 0 到 0.5 的原则，最终锁定了 chrome 插件这个小赛道，基本只需要 javasrcip+css 一些前端知识+服务器的知识（其实真做起来，还是有很多盲区），就能做 

 

出来一个产品。另外这种小产品，一般只专注解决一个小需求即可。同时审核也快（差不多 12 个小时才审核上线，之前看一些资料，审核很快的）。

二，选细分市场或需求

选哪个细分市场或需求，其实跟跨境选品一样，往往新人觉得是玄学，其实你真动手做了第 1 个小产品，然后慢慢就会有感觉，但是你整天想这想那，那很大概率，就没有然后的然后了。

其实这次小工具选品，也还是走了一些固有的思维的弯路，例如最早有两条大路，电商类小工具，或 wp+woo 小工具，但其实等于没有，因为没有办法立马就干，还有开发人员的选择（在这里浪费了很多时间......后面再讲）。最后，是一美国的做物流的朋友，她有个小需求，即 pdf 相关的需求，最后付费这里也是（半买半送，后面相关的 pdf 需求 PDFXYZ（暂时隐去插件名字，后面有公开，因为上架有一段时间），都会免费送给她一整套小插件使用）。付了两笔 49.99 美金（钱不多，但至少有个正向反馈，这个最重要）。

 

 

![](img/chanpin-bianxian_0887.png)

最终选 PDFXYZ 这个细分需求，还有几个原因，你可以细品一下，尤其是想做一个新市场，找个细分点，快速试一下，小成本跑通整个流程，即完成大于完美。当然还有 deadline 的作用（这个对于小众产品或市场，太重要了，开发进度一拖，各种成本就上来了）。

另外这个 PDF 需求，在 github 找到相关的实现源码（虽然是其它语言的，但对于 chrome 插件也是可以复用的），即可以借前人的轮子来用，加快整个进度。

PDF 各种需求，在国外市场是巨大的，直接 Google 一下，居然有 250 多亿的搜索结果。因为软件是边际效应的，你开发出来，其实后面的维护成本很低的。另外这个需求，也是为了先试 chrome 插件市场，还有积累原始的 pdf 需求的第 1 批种子用户。因为周边需求的拓展太多了。每个子功能，都是可以做成一个小工具的，即形成了小工具矩阵（是不是有点跨境的多账号味道了）。

 

 

![](img/chanpin-bianxian_0892.png)

三，想与做的各种坑

**3.1 **招人坑

这里浪费了好多时间，一是具体需求没有太多确定，就去招人，而且还是在国外平台上，一是 fiverr，二是 upwork 等 freelancer 平台。

有些事，只有你真正做过了，才知道这里的坑有多少。就像这个 Chrome 插件 PDFXYZ，看似简单，里面还有几个难点需要一定经验，或者是主动解决问题能力的程序员才能搞定。

 

 

而找老外做开发，你得 1，2，3，4，5........把实现细节拆分才行。要不然，加上时差，还有技术框架不熟悉（我的那些编程语言，算法套路基本都交还给大学老师了），这一来一回，更是难上加难了。

如果你要找老外做开发，一定得先列好细的需求，直接让他实现 code 就好了。要不然开发时间和进度会拖死你。最重要的是，多找几个来对比，多磨合几轮，才能找到合适自己的。

最后找了两个朋友（朋友 L，一直有帮我处理程序上一些事，全栈能力有，但需求时间来实现；朋友 Y，是另外一个朋友介绍的，大公司的前端大牛）来做两个版本，同样的需求。为什么要这样做呢？因为我不只做这一个插件或小工具，后面还会有 N 多（如果你有程序员朋友想变现，也可以推荐给我），前面已经多次提到，开发时间对于小工具来说是个大坑，如果托得时间越久，那成本只增不减。也是相互一个磨合过程，开发这个活，还是技术优势来主导的，差一点，就真的需要时间去打磨，别无他法。

**3.2 **业务流程坑

做小众市场先行原则：找别人已经赚了钱的需求，再深挖（最直接的是找差评，看看能不能解决这些问题），你离变现不会太远。

有句话叫，你想学会游泳，你至少得下一次水吧，要不然动作再漂亮也没有什么用。先行原则，前面已经提到过了，即 pdf 这个大工具，周边其实是有很多需求的，用户基数也足够大，先积累种子用户，能收到第 1 块的用户那更好。再去拓展其它需求，赚钱是迟早的事。先下水，那就直接先模仿，把核心需求实现，尤其是支付环节实现（chrome 插件之前还有 google pay 的支付，现在没有官方支付支持了，但是能接第 3 方，这里支付坑再展开讲一下）。

 

 

讲一下 PDFXYZ 这个小工具，核心需求，朋友 L 是用中间服务器来实现的，PDF 文件基本无损来承现了（即文件清晰度，因为 pdf 文档，要么是文字，要么是图片，还有其它格式合成的），即能满足客户真实需求，但这里面还有服务器上传下载的问题，还有文件大小的门槛（文件大，下载时间就长）。文件大了，插件的体验就极差了，因为会卡在那里，半天动不了，只有限制其大小，设置为 10M。

朋友 Y，是直接用 js api 来实现，但是文件下载下来就模糊（客户的核心需求实现还差一些），另外同样的，也是文件上传下载的问题，这种文件大小限制就大一些，为 30M。

**3.3 **支付坑（大坑）

国外的工具或一些需求，或产品，除了广告变现以外（Google Adsense）；常用的变现方式：捐赠（paypal）；还有通过分享产品等知识，用 affiliate 模式（分销赚佣金）来实现；那最直接的方式，就是直接收费。

chrome 插件大多数情况下，只能选择捐赠，或直接收费的方式。结果现在的 Paypal 账号是不支持国内账号的捐赠。

直接收费方式，因为 google pay 官方支付停止，但接受第 3 方支付。你可能直觉是 Paypal，但不好意思，虚拟产品，Paypal 不支持（应该大型软件会有收款白名单）。还有其他选择：stripe 等（但现在申请，又是门槛 N 高，申请下来，也会被封号的风险）。

现在收款，是先试的是 Sendowl（可以再转 Paypal，现在测试的结果，几十美金，通过 sendowl 付款链接，Paypal 是直接到帐的）（这个工具是壹树老板（插件大佬，公众号：

树下随想）推荐，尤其是支付这个环节，帮了老忙了）。这里壹树老板也趟了无数的坑（如果你想问，请付费，真的绝对超值）。

 

 

因为 sendowl 是 web 端网页支付，插件端要有个支付回传（webhooks），确认用户已经支付成功。熊（全栈大牛，大学同学，之前的公众号有介绍过）+壹树老板的综合建议：

不做登录就可以整个本地的唯一标识 Key，当用户付款了，就生成一个标识 Key，保存到数据里（或者用户本地电脑缓存）；另外最好手动或自动再发一下支付邮箱一封邮件，把其 Key 发给用户。如果用户卸载了，就可以用这个 Key 来识别。

另外插件内是不支持回传确认的，如下图，即卡死在那里，因为没有回传确认是否支付成功。朋友 Y 是直接用的单独新开浏览器标签页，让付款用户直接通过 sendowl 网页链接付款。

![](img/chanpin-bianxian_0905.png)

 

 

**3.4 **图标图像坑

这个坑，估计大多数独立开发者，只有真的有一款小工具跑出来后才会意识到，但往往这个时候，估计你的款都有可能被扣光，如果造成侵权的话。

前文有提到是 PDF 的需求，图标，朋友 Y 就直接用了 Adobe pdf 的图标，虽然辨识度极度，但这个潜在的小隐患，可能让你全盘皆输。

也许你没有碰到过，所以，看到这个坑，会不会有夸大的嫌疑。真没有，想起 N 前年，第 1 次私模，做硅胶材质的汉堡制作工具，因为一家加拿大公司把这个细分类的常用词都注册成商标了，导致当时在亚马逊仓库的货、在途的、工厂生产的，都得换包装（还是彩盒），产品上的 LOGO 产品词得去掉，这样一处理，小几十万没有了。。。。。。

**3.5 **插件上架坑

（细节见最后的第四大部分内容：运营推广复盘）力求真实最好。

**3.6 **推广坑

（详情如上<3.5>，因为是虚拟产品，直接 chrome 插件网页地址是可以投 google 的搜索广告，但是联盟广告是不行的，需要另外做网站，但 PDF 这个需求，其实投联盟广告是极好的，尤其是定点投放相关网站）。另外有尝试 native ads(zeropark, propellerads)，google ads（直接 chrome 插件网页可投 google 搜索+智能广告），bing ads 被否，quora ads 被否。

 

 

暂时算是盲测阶段，没有安装统计代码（因为插件不同于网页，具体可参考

https://developer.chrome.com/docs/extensions/mv2/tut_analytics/），google ads 也只是做了简单优化：需求地点（直接定位到城市）、设备（排除掉非电脑 PC 端）、keywords 直接上精确匹配.......

简单优化的数据，表现最好的区域为新加坡，0.5-0.7 美金一个安装，精细化优化，成本至少可以降一半以上。30%的卸载（数据量基数不大），另外同类产品功能差不多的情况下，是免费的，PDFXYZ 这个小工具性能也要再优化。安装率 45%，即差不多 2 个人看，有 1 个安装，即需求还是有的，流量也算精准。

下面的 20 年国外的一份统计表，值得你在 chrome 插件，初始预算要花到多少钱。到了 1000 的用户数，你基本算是脱颖而出，当然，现在 21 年，用户基数的标准提高了。如果按照前面的简单优化的单个安装成本 0.5-0.7 美金，你推广试错成本至少得你准备 500 美金，是不是突然发现这个事可以干那么一下子了。

![](img/chanpin-bianxian_0914.png)

**3.7 **营销坑

 

 

（这里主要是插件定价，还有后面的插件体系布局的事，即形成老用户闭环，积累可触达的可营销的客户邮箱列表，你前面的推广成本才被摊薄。具体内容详见<3.5>）评论区：

暂无评论
