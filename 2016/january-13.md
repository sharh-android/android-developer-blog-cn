# Cardboard SDK现已集成环绕音频

> wizChen翻译 原文地址[http://android-developers.blogspot.jp/2016/01/spatial-audio-comes-to-cardboard-sdk.html](http://android-developers.blogspot.jp/2016/01/spatial-audio-comes-to-cardboard-sdk.html)

来自Nathan Martz，谷歌Cardboard产品经理

人类可以听到来自四面八方的声音-比如当消防车开过或者是飞机飞过你头顶的天空。从今天开始，Cardboard 已经为大多数和安卓设备支持的音频开放了SDK，所以你可以开发让人同感身临其境的虚拟现实的应用。而这一切，用户只需要有一部智能机，一套常规的耳机和一个Google Cardboard。


### 你听到声音的方式

许多应用只是简单的开发了音频的功能-用单独的左右声道播放声音而已。但是随着今天SDK的升级，开发出的应用将真正的让用户听到真实的声音，例如：

- SDK将利用生理学的侦听器和虚拟声源的位置来确定用户所听到的。例如：来自右边的声音到达用户左耳会稍有延迟，而且高频元素会更少(通常是由头骨决定的)
- SDK允许你自己决定虚拟环境的大小和材料，而这两个因素都是决定发出声音的质量的。所以你会发现在一个紧闭的空间和一个大的地下室发出的声音是大有不同的。


### 针对智能机优化

我们在理想范围内构建了今天的SDK，将性能发挥的更好，让你的应用增加的音频最小的对CPU（你的许多应用运行的地方）产生其他不良影响。我们总结了这么几条方式：

- SDK是为手机CPU（比如SIMD架构的）特殊优化的，实际计算实时音频实在另外单独线程执行的，所以大部分的处理都是在主CPU之外。
- SDK允许你控制每一个声音的保真度。因此，你可以分配你的更多精力到声音处理上，而不是强调其他人。


### 简单，本地集成

SDK新的音频功能真的很容易上手。开发团队可以用一组全面的组件创建Android，iOS，Windows和OS X系统上的音景。原生的Android开发者可以使用一个简单的Java API，用于模拟虚拟的声音和环境。

![开发人员体验空间音频的样例应用](http://2.bp.blogspot.com/-yH-RHvnjbNg/VpaEAv2xsPI/AAAAAAAABU8/E2bRFQmk5ug/s640/image00.png)

查看我们的[Android示例应用程序](https://github.com/googlesamples/cardboard-unity/blob/master/Samples/SpatialAudio/AudioSpaces.apk?raw=true)（仅供开发人员参考），浏览Cardboards在开发者网站上的[文档](https://developers.google.com/cardboard/unity/guide?utm_campaign=cardboard_discussion_spatialaudio_011316&utm_source=anddev&utm_medium=blog#spatial_audio_for_vr)，今天就开始体验新的SDK和空间音频吧。我们非常期待你能开发出耳目一新和绝佳的应用！ 
