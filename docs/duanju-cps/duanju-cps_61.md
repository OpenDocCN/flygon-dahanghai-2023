# 6.3.2.1 素材片段分割

Step1，将短剧全集导入剪映，复制主轨道中的全部视频（Ctrl+C），粘贴到副轨道（Ctrl+V），并将副轨道中的素材合并为一个片段（选中副轨道所有素材，右键，点击“新建复合片段”）。

[1.1.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/IilUbNinloALaKxRlk8c1Ldinsf)

Step2，对副轨道添加蒙版（右上角蒙版-镜面），将蒙版调整到遮挡字幕的位置和粗细，最后对副轨道添加模糊特效（特效-画面特效-基础-模糊），将模糊特效拖动到副轨道，设置模糊度为 20-40（在遮住原字幕和不影响无字幕区域观看体验两个标准下适当调整）。

[1.2.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/GvXRbqPRMoHYVxxgT4YcqYLln1d)

Step3，从头到尾拖动进度条，检查模糊的副轨道蒙版是否遮挡住所有字幕，如果全部遮挡，进入 Step4；否则，将未遮挡住字幕的部分的副轨道分割出来（选中副轨道，将进度条放到未遮挡住字幕的片段开头和结尾各按一次 Ctrl+B（分割操作的快捷键）），调整未遮挡住字幕部分模糊蒙版的上下位置，再进入 Step4。

[1.3.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/SJWwbK9lboI3agxRvqLcddrvnxe)

Step4，创建文件夹“模糊原字幕”，将视频分段导出到该文件夹（以 30 集一段为例，将进度条放在第 1 集开头，按键盘上的“I”键，再将进度条放到第 30 集结尾处，按键盘上的“O”键，这一步是用 I/O 快捷键将导出时间范围限制在 1-30 集内，最后按右上角“导出”按钮，导出设置中选择 720P，更低的码率，24fps 的帧率来减少剪映及后续软件的处理时间，命名为 01-30）。

对 Step3 中调整过蒙版位置的片段，单独导出即可。

这里有个进阶操作，可以将副轨道先按照 1-30，31-60 的区间分割好（选中副轨道，将时间轴拖到在 30/60 集的结尾处，按 Ctrl+B 做分割操作即可），导出的时候只要选中副轨道 1-30 集对应的片段，按 Shift+X，这样就能将导出范围限制为 1-30 集，然后再按导出键即可。

[1.4.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/YdYtbaKbpoiMPYxENJxcrBAJnYg)

Step5，创建文件夹“提取字幕”，将副轨道隐藏，更改导出目标文件夹为“提取字幕”，再次导出视频，这部分视频后续用于字幕的提取。

[1.5.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/WMmlb4K6woWQj7xi8oBcduy4n3T)

Step6，打开 VSE（硬字幕提取软件），选择文件夹“提取字幕”中的文件，调整字幕识别区域，点击开始识别字幕。一般建议选择该软件的快速识别模式，速度相对较快（大概 20 分钟就能识别 30 集合集，具体速度和电脑配置挂钩），缺点是可能会漏掉极少量的字幕。

对提取出的字幕存在的漏字幕和极个别错别字问题，可以在 Step7 精修字幕时进行更正，也可以在后续要用到字幕有问题的片段时再进行手动修正。

这一步将内嵌字幕提取为 srt 外挂字幕，也可以使用其他基于 OCR 图像识别的内嵌字幕提取工具，例如付费软件 Videosrt Pro（性价比很高，如果 VSE 软件不能正常运行，可以试着用这个软件代替 VSE 进行这一步的操作，VideoSrt 开源地址 [`github.com/wxbool/video-srt-windows`](https://github.com/wxbool/video-srt-windows)）。

[1.6.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/JUhSbaQKeoIWZ5xq0kec7m2wnGg)

Step7，创建文件夹“精修字幕后”，将 VSE 提取的字幕和“模糊原字幕”中对应的视频文件导入到剪映。对视频文件进行镜像操作。

将字幕导入轨道中（注意开头要和视频文件开头对应好）调整字幕的风格大小缩放，将字幕移动到被模糊蒙版遮挡的位置。之后点击任意字幕，在右上角的字幕窗口检查是否有过长的字幕，如果有，可以在该字幕最后一两个字之前按下 Enter 回车键即可。

导出精修字幕后的视频和字幕文件（点击右上角导出，导出设置中选择勾选字幕导出）。

[1.7.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/TpvebEoFNoVJVzxhU5BckeTQnUf)

Step8，打开大拍档剪辑助手（按字幕分割视频的软件）的素材裁剪器功能（APP-素材裁剪器），导入 Step7 中精修字幕后的视频，点击自动分割裁剪，选择按字幕分割，选择 Step7 中生成的字幕文件，选择分割方式一“用于文件名被搜索”，点击分割，再点击右下角“裁剪设置”，都按照默认设置确定即可，导出分割好的视频。

新建文件夹“分割后片段”，将分割好的视频移动到该文件夹中。

[1.8.mp4](https://search01.shengcaiyoushu.com/upload/doc/SUYad816hofSjmxGHeWcbjoEnpc/CbfvbpbvooOWqEx0f2KcMEEwnAO)

执行完 Step1-Step8，就完成了素材片段分割的工作。