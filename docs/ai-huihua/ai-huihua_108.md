# 6.1 深度了解描述词

为了让大家在各个工具中能够顺利完成出图，前面我们零散提过一些描述词的写法。

但实际上，描述词是一门值得细细推敲的学问，也是我们做好 AI 绘画的核心。所以我们来深度了解一下，描述词还有哪些需要注意的要点。

描述词的分类

•画质•(masterpiece),(the best quality),extremely detailed , ultra high res, best quality, photo, 4k, (photorealistic:1.4),

•主题/场景•Indoor, outdoor, grass

•人物属性特征•头发长短、颜色、脸部、头饰、装饰、服装：hair length， hair color， hair style， decorations on head•姿势角度等•pov_hands,sitting,the_whole_body•look at, look up, look down, bird 's-eye view

•物体•book,cloud,gun,pen,teacup

•时间光线•day,evening,morning,night,twilight•rim light, Warm light, soft light,back light

•画风•cartoon, streampunk, Disney style

•艺术家•Van Gogh, Hayao Miyazaki

•镜头•depth of field,

•模型引入等

描述词书写方式

•词语：1girl， smile， street

•句子：A smiling girl， walking in the street

•短语：A girl is walking down the street with a smile and an ice cream in her hand

•Emoji: money-mouth face,smiling face with hearts,smiling face with heart-eyes•参考—>[`unicode.org/emoji/charts/emoji-list.html`](https://unicode.org/emoji/charts/emoji-list.html)

•颜文字：o_O 这种•参考—>[`zh.wikipedia.org/wiki/%E8%A1%A8%E6%83%85%E7%AC%A6%E8%99%9F%E5%88%97%E8%A1%A8`](https://zh.wikipedia.org/wiki/%E8%A1%A8%E6%83%85%E7%AC%A6%E8%99%9F%E5%88%97%E8%A1%A8)

•分隔：不同的描述词中间用英文逗号隔开，有空格和换行不影响

•同一类描述词：如 blonde hair， blue hair（金色头发和红色头发）会分别或者混合出现

•用 AND 把多种要素都融进去进去（用 AND 要素都能出现，逗号不一定）•例：blonde hair AND blue hair（AND 必须是大写）

•正描述词：你想让 AI 帮你生成图片的描述词，可以是单词，也可以是句子，中间用逗号隔开，用英文描述。如我们前文出现过的 1girl， long hair；•通用：masterpiece，the best quality•大致顺序（画面质量提示词）， （画面主题内容）（风格）， （相关艺术家）， （其他细节）例如：（masterpiece），（best quality），（ultra-detailed）， （full body:1.2）， 1girl，chibi，cute， smile， white Bob haircut， red eyes， earring， white shirt，black skirt， lace legwear， （sitting on red sofa）， seductive posture， smile， A sleek black coffee table sits in front of the sofa and a few decorative items are placed on the shelves， （beautiful detailed face）， （beautiful detailed eyes），

•负描述词：不想让 AI 在图片上出现的描述•通用：extra arms， disfigured， deformed， cross-eye， body out of frame，NSFW， （worst quality:2）， （low quality:2）， （normal quality:2）， lowres， normal quality， （（monochrome））， （（grayscale））， skin spots， acnes， skin blemishes， age spot， （ugly:1.331）， （duplicate:1.331）， （morbid:1.21）， （mutilated:1.21）， （tranny:1.331）， mutated hands， （poorly drawn hands:1.5）， blurry， （bad anatomy:1.21）， （bad proportions:1.331）， extra limbs， （disfigured:1.331）， （missing arms:1.331）， （extra legs:1.331）， （fused fingers:1.61051）， （too many fingers:1.61051）， （unclear eyes:1.331）， lowers， bad hands， missing fingers， extra digit，bad hands， missing fingers， （（（extra arms and legs）））

描述词的权重：简单说就是优先级，AI 对描述词处理的优先级

•权重写法•（word） - 将权重提⾼ 1.1 倍•例：（best quality），（masterpiece）•（（word）） - 将权重提⾼ 1.21 倍（= 1.1 * 1.1）（多个括号就是继续*1.1）•例：（（masterpiece））•[word] - 将权重降低 90.91%•例：[flower]•（word:1.5） - 将权重提⾼ 1.5 倍•例：（long skirt:1.5）•（word:0.25） - 将权重减少为原先的 25%•例：（long skirt:0.25）•\（word\） - 在提示词中使⽤字⾯意义上的 （），让 AI 理解这个不是加权重的意思•常见出现在写作者或者是风格描述上•字符提示词越多，个词权重越⼩

描述词替换（渐变）

•[to:when] == [关键词：数字] •在生成图片的过程中增加这个关键词进去

•[from::when] == [关键词：:数字] • 在生成图片的过程中删除这个关键字•数字大于 1—>表示步数 例如[bow tie:12] 第十二步的时候就不使用这个关键词了。

•[from:to:when] == [关键字 1:关键字 2:数字] •数字大于 1 表示从第多少步之前用关键字 1，之后就变成执行关键字 2•数字小于 0 表示百分比，例如 0.5—>表示 50%之前用前面的关键字，步数达到 50%以后用后面的关键字

循环实现关键字

•[关键词 1|关键词 2|关键词 3] == [a|b|c]

•轮流使用关键词生成，如第一步生成 a，第二步 b，第三步 c，第四步 a 这样循环

模型调用（LORA 等）

•LORA• <lora:模型名称：权重>• 例：<lora:blindbox_V1Mix:1>，权重可以调整，数值越小，使用率越低，建议最大不超过 1•lora 可以同时使用多个，多个 lora 的权重总和建议不要大于 1.3，不然图片上的画面容易崩掉～

•Embedding•直接在模型处点击即可调用•模型不能放到负描述词中！！！

注意点

•不要有错误的单词，会被乱识别

•用词尽量具体，不要模糊广泛，避免随机性太大

•受权重影响，读取顺序—>从左到右，越到后面权重越小

![](img/e12d1c8b9f4ffdf6c4edf913cceed533.png)