# Mac中的Shadowsocks客户端

Mac下的Shadowsocks客户端也有不止一个。

用过的有：

![ShadowsocksX和ShadowsocksX-NG的图标](../../assets/img/shadowsocksx_shadowsocksx_ng_logo.png)

* `ShadowsocksX`
  * 对应下载地址是：[ShadowsocksX-2.6.3.dmg]([https://github.com/shadowsocks/shadowsocks-iOS/releases/download/2.6.3/ShadowsocksX-2.6.3.dmg])
* `ShadowsocksX-NG`
  * 之所以换用ShadowsocksX-NG：
    * 后来在shadowsocks.to改用新加密算法`chacha20-ietf-poly1305`后，而ShadowsocksX不支持，所以才换用`ShadowsocksX-NG`的。

两个版本的功能和使用方式，基本上没太大区别。

下面主要来介绍ShadowsocksX-NG的使用。

## Mac版ss客户端：ShadowsocksX-NG

### 下载和安装ShadowsocksX-NG

从Github中下载：[官网（可能访问不了）](https://github.com/shadowsocks/ShadowsocksX-NG/releases)
或者：[科学上网下载](https://kxsw2019.cf/guide/mac.dmg)
![GitHub中下载ShadowsocksX-NG](../../assets/img/github_download_shadowsocksx_ng.jpg)

解压下载得到的`ShadowsocksX-NG.1.7.0.zip`得到app文件：`ShadowsocksX-NG.app`

把ShadowsocksX-NG.app拖动到应用程序Application文件夹，即可：

![安装ShadowsocksX-NG](../../assets/img/drag_shadowsocksx_ng_to_application_folder.png)

## 运行ShadowsocksX-NG

安装后，从LaunchPad中：

![Mac中LaunchaPad打开ShadowssocksX-NG](../../assets/img/mac_launchpad_shadowsocksx_ng.jpg)

或从 应用程序中也可以找到：

![Mac中应用程序中的ShadowssocksX-NG](../../assets/img/mac_app_shadowsocksx_ng.png)

Shadowsocks-NG，点击以启动：

当前Shadowsocks-NG的版本是最新的1.7.0:

![ShadowssocksX-NG最新版本1.7.0](../../assets/img/shadowsocksx_ng_1_7_0.png)

## ShadowsocksX-NG中添加服务器配置信息




### 通过扫描二维码添加

 
#### 可以在网站【我的账号】中找到二维码



会弹出二维码：

![弹框显示ss的二维码](../../assets/img/popup_show_ss_qrcode.jpg)

然后点击`ShadowsocksX-NG的菜单` -> `扫描屏幕上的二维码`

![ShadowsocksX-NG的扫描二维码](../../assets/img/menu_scan_ss_qrcode.png)

会自动识别屏幕上（刚才页面中弹出的）二维码，扫描成功后会提示：

![已添加新Shadowsocks服务器配置](../../assets/img/added_new_shadowsocks_server_config.png)

### 手动方式

点击 `服务器 - xxx` -> `服务器配置`

![ShadowsocksX-NG的服务器配置](../../assets/img/shadowsocksx_ng_server_config.jpg)

会弹出设置界面，点击左下角的加号➕，然后填入对应配置信息：

![ShadowsocksX-NG手动填写ss服务器配置](../../assets/img/shadowsocksx_ng_manual_fill_config.png)

* 地址：[必填]服务器的IP或域名地址
  * 对应着shadowsocks.to提供的：`节点服务器地址`
* 端口：[必填]端口号
  * 对应着shadowsocks.to提供的：`服务端口`
* 加密方法：[必填]（现在最新的加密方法是）`chacha20-ietf-poly1305`
  * 对应着shadowsocks.to提供的：`加密方式`
* 密码：[必填]密码
  * 对应着shadowsocks.to提供的：`登录密码`
* 备注：[选填]
  * 自己填个自己觉得容易识别的好记的名字
  * 比如： hk1

然后点击确定。

用同样方法，一个个的去添加其他的服务器配置。

## ShadowsocksX-NG其他使用相关的配置

在添加了ss的服务器之后，接着去介绍如何使用ShadowsocksX-NG客户端。

### 打开/启用Shadowsocks

先去打开SS的客户端，选择`打开Shadowsocks`

![ShadowsocksX-NG打开Shadowsocks](../../assets/img/shadowsocksx_ng_enable_shadowsocks.png)

如此，即可去畅游互联网了，可以去打开本来无法访问的而现在可以访问的，比如：

https://www.youtube.com

![科学上网后打开youtube](../../assets/img/after_ss_access_youtube.jpg)

当然，下面还是可以去根据需要去更改对应的设置的：

### 选择工作模式

如果不想要看下面的模式的详细解释，那么直接使用默认的`PAC自动模式`即可。

关于不同工作模式的解释：

* `PAC自动模式`
  * 让Shadowsocks-NG去（根据设置中的GFW List）自动识别在打开网页时，是否需要翻墙
    * **推荐：普通小白用户使用此模式**
    * 比如打开国内的百度，腾讯，网易等网站，不需要翻墙
    * 比如打开国外的google，youtube等需要翻墙
  * ![ShadowsocksX-NG选择PAC自动模式](../../assets/img/shadowsocksx_ng_choose_pac_auto_mode.png)
* `全局模式`
  * 强制对于所有打开的网页都是用翻墙
    * 优点和使用场景：对于部分页面，有些网页用自动模式打不开，则可以尝试全局模式，往往可以打开
    * 缺点：如果对于本身无需翻墙的国内网站，比如百度也强制翻墙的话，访问速度可能会降低
* `手动模式`
  * 提示：一般人很少用
  * 设置为手动模式后，需要自己去`编辑PAC用户自定规则`，添加自己定义的规则，决定哪些页面翻墙，哪些页面不翻墙。

### 选择用哪个服务器去翻墙

在添加了多个服务器后，可以点击 `服务器 - xxx` -> 去选择切换为自己需要的服务器：

![ShadowsocksX-NG从hk1的ss服务器](../../assets/img/shadowsocksx_ng_from_hk1_ss_server.jpg)

即可切换到（自己平时经常使用的，觉得速度和稳定性都不错的）us2的服务器：

![ShadowsocksX-NG切换到了us2服务器](../../assets/img/shadowsocksx_ng_switched_to_us2.png)

### 设置开机启动

想要每次开机自动启动的话，可以去：`偏好设置`

![ShadowsocksX-NG的偏好设置](../../assets/img/shadowsocksx_ng_preferences.png)

勾选上`开机启动`

![ShadowsocksX-NG中勾选开机启动](../../assets/img/shadowsocksx_ng_select_run_on_boot.png)


