&emsp;&emsp;本文内容整理自[uni-app官方教程](https://uniapp.dcloud.io/)。

&emsp;&emsp;[uni-app](https://uniapp.dcloud.io/)是一个使用Vue.js开发跨平台应用的前端框架，开发者编写一套代码，可编译到iOS、Android、H5、小程序等多个平台。

&emsp;&emsp;uni-app框架由[Dcloud](https://www.dcloud.io/)即数字天堂(北京)网络技术有限公司推出，该公司主要产品有Web开发IDE Hbuiler、HbuilderX，前端框架mui、uni-app，增强版的手机浏览器引擎H5plus等。

![](https://upload-images.jianshu.io/upload_images/2783386-33e826149b5a7f82.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 一、环境搭建
&emsp;&emsp;使用 `HBuilderX`可视化界面快速创建项目，HBuilderX内置处理了相关环境依赖。

&emsp;&emsp;HBuilderX：IDE。[最新版本下载地址](http://www.dcloud.io/hbuilderx.html)
&emsp;&emsp;微信开发者工具：调试预览工具。[最新版本下载地址](https://mp.weixin.qq.com/debug/wxadoc/dev/devtools/download.html)


### 二、创建uni-app项目

&emsp;&emsp;点击工具栏里的文件 -> 新建 -> 项目：

![](http://upload-images.jianshu.io/upload_images/2783386-e2435fb81aa15f9c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;选择uni-app，输入工程名，如：hello-uniapp，点击创建，即可成功创建 uni-app。点击模板里的 Hello uni-app 即可体验官方示例。

![](https://upload-images.jianshu.io/upload_images/2783386-32baf1f3d909de03.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



### [三、运行uni-app](https://uniapp.dcloud.io/quickstart?id=%e8%bf%90%e8%a1%8cuni-app)

&emsp;&emsp;1.  真机运行：连接手机，开启USB调试，进入hello-uniapp项目，点击工具栏的运行 -> 真机运行 -> 选择运行的设备，即可在该设备里面体验uni-app。

![](http://upload-images.jianshu.io/upload_images/2783386-4ca616f7f1898b99.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;2.  浏览器运行：进入hello-uniapp项目，点击工具栏的运行 -> 运行到浏览器 -> 选择浏览器，即可在浏览器里面体验uni-app 的 H5 版。

![](http://upload-images.jianshu.io/upload_images/2783386-e99c2d99105536fa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;3.  在微信开发者工具里运行：进入hello-uniapp项目，点击工具栏的运行 -> 运行到小程序模拟器 -> 微信开发者工具，即可在微信开发者工具里面体验uni-app。

![](http://upload-images.jianshu.io/upload_images/2783386-34b124fd2549bd5e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### [四、uni-app调试](https://uniapp.dcloud.io/snippet?id=%e4%bd%bf%e7%94%a8-chrome-%e8%b0%83%e8%af%95)
#### [1.使用 Chrome 调试](https://uniapp.dcloud.io/snippet?id=%e4%bd%bf%e7%94%a8-chrome-%e8%b0%83%e8%af%95)

&emsp;&emsp;进入 `uni-app` 项目，点击工具栏的运行 -> 运行到浏览器 -> 选择 Chrome，即可将 uni-app运行到 浏览器，可参考 [运行uni-app](https://uniapp.dcloud.io/quickstart?id=%e8%bf%90%e8%a1%8cuni-app)，运行到浏览器后，就能和普通 web 项目一样进行预览和调试了。

&emsp;&emsp;**注意**：Chrome调试只能保证样式一致，部分原生能力是不支持的。

&emsp;&emsp;点 Chrome 控制台的 Sources 栏，可以给 js 打断点调试。

&emsp;&emsp;在 Page 下找到 webpack 里的工程目录，可直接找到对应的vue页面进行断点调试；或按 Ctrl+P搜文件名，进入页面调试；也可点击控制台的 log 信息，进入对应的页面进行调试。

![image](http://upload-images.jianshu.io/upload_images/2783386-bc4a2426832d7a92.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image](http://upload-images.jianshu.io/upload_images/2783386-efff56c8f130728a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### [2.使用微信web开发者工具调试](https://uniapp.dcloud.io/snippet?id=%e4%bd%bf%e7%94%a8%e5%be%ae%e4%bf%a1web%e5%bc%80%e5%8f%91%e8%80%85%e5%b7%a5%e5%85%b7%e8%b0%83%e8%af%95)

&emsp;&emsp;`uni-app` 运行到微信web开发者工具，可在控制台查看 `console` 信息，网络请求等信息等。

&emsp;&emsp;**注意**：开发App或微信小程序均可使用微信开发者工具进行调试。

&emsp;&emsp;页面样式调试和一般的web项目一样，通过调试的箭头选中元素即可查看相应的节点和样式，如下图：

![uni-app](http://upload-images.jianshu.io/upload_images/2783386-a1383b02b8d819f8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;调试 js 时需要切换到 Sources 栏，选中想要调试的那个页面的js，进行调试（如果js代码是压缩过的，点击右下角的{}可格式化代码），如下图：

![uni-app](http://upload-images.jianshu.io/upload_images/2783386-424fbda77dca4c6b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###  [五、发布 uni-app](https://uniapp.dcloud.io/quickstart?id=%e5%8f%91%e5%b8%83-uni-app)

#### [1.打包为原生App（云端）](https://uniapp.dcloud.io/quickstart?id=%e6%89%93%e5%8c%85%e4%b8%ba%e5%8e%9f%e7%94%9fapp%ef%bc%88%e4%ba%91%e7%ab%af%ef%bc%89)

&emsp;&emsp;在HBuilderX工具栏，点击发行，选择原生app-云端打包，如下图：

![](http://upload-images.jianshu.io/upload_images/2783386-ab64aeb5751ddeed.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;出现如下界面，点击打包即可。

![](http://upload-images.jianshu.io/upload_images/2783386-a3daaeea10d64a4c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### [2.打包为原生App（离线）](https://uniapp.dcloud.io/quickstart?id=%e6%89%93%e5%8c%85%e4%b8%ba%e5%8e%9f%e7%94%9fapp%ef%bc%88%e7%a6%bb%e7%ba%bf%ef%bc%89)

&emsp;&emsp;`uni-app` 支持离线打包，在 HBuilderX 生成离线打包资源，然后参考 [离线打包](http://ask.dcloud.net.cn/docs/#//ask.dcloud.net.cn/article/104)（或参考其他用户写的 [离线打包日记](https://ask.dcloud.net.cn/article/35302)），即可进行离线打包。

&emsp;&emsp;在HBuilderX工具栏，点击发行，选择本地打包，如下图，点击即可生成离线打包资源。

![](http://upload-images.jianshu.io/upload_images/2783386-e7fa290c805fc966.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### [3.发布为H5](https://uniapp.dcloud.io/quickstart?id=%e5%8f%91%e5%b8%83%e4%b8%bah5)

&emsp;&emsp;1.  在 `manifest.json` 配置发行后的路径（发行在网站根目录可不配置），比如发行网站路径是 www.xxx.com/html5，在 `manifest.json` 文件内编辑 `h5` 节点，`router` 下增加 `base` 属性为 html5，如下图所示：

![](http://upload-images.jianshu.io/upload_images/2783386-9cc73c696b46e2ce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;2.  在HBuilderX工具栏，点击发行，选择网站-H5手机版，如下图，点击即可生成 H5 的相关资源文件，保存于 unpackage 目录。

![](http://upload-images.jianshu.io/upload_images/2783386-8837b20b548ee260.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### [4.发布微信小程序](https://uniapp.dcloud.io/quickstart?id=%e5%8f%91%e5%b8%83%e5%be%ae%e4%bf%a1%e5%b0%8f%e7%a8%8b%e5%ba%8f)

按照如下步骤可将 `uni-app` 发布到微信小程序：

&emsp;&emsp;1.  申请微信小程序AppID，参考[微信教程](https://developers.weixin.qq.com/miniprogram/dev/#申请帐号)
&emsp;&emsp;2.  在HBuiderX中，打开manifest.json，如下图所示配置小程序AppID

   ![](http://upload-images.jianshu.io/upload_images/2783386-0783efc797a5edb4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

&emsp;&emsp;3.  在HBuilderX中顶部菜单依次点击 "运行" --> "运行到小程序模拟器" --> "微信开发者工具"，等待 `uni-app` 项目成功编译并自动启动微信开发者工具

&emsp;&emsp;4.  在微信开发者工具中，测试项目代码运行正常后，点击"上传"按钮，之后按照 "提交审核"--> "发布" 小程序标准流程，逐步操作即可，详细查看[微信官方教程](https://developers.weixin.qq.com/miniprogram/dev/quickstart/basic/release.html)

###  六、项目代码
&emsp;&emsp;反馈星是使用uniapp开发的上报工具类项目。
&emsp;&emsp;发送文字、图片、音频、视频内容，您将获得意想不到的反馈。

&emsp;&emsp;Github下载：https://github.com/XieXiePro/FeedBackStar

