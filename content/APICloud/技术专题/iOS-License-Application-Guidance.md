/*
Title: iOS证书申请教程
Description: iOS证书申请教程
Sort: 12
*/

[云编译p12证书制作](#1)

[创建App ID](#2)

[添加测试设备](#3)

[云编译mobileprovision证书制作](#4)	

[推送证书制作](#5)

#**云编译p12证书制作**<div id="1"></div>

##生成certSigningRequest文件

如图，打开应用程序->实用工具->钥匙串访问

![图片说明](/img/docImage/227.png)
 
如图，选择从证书颁发机构请求证书

![图片说明](/img/docImage/228.png)

接下来填写邮件地址，选择存储到磁盘，点击继续

![图片说明](/img/docImage/229.png)
 
如图，保存文件到桌面。

![图片说明](/img/docImage/230.png)

##制作p12证书

首先打开苹果开发网站，通过Member Center进入开发账户，如图：

![图片说明](/img/docImage/231.png)
 
然后选择Certificates, Identifiers & Profiles，如图：

![图片说明](/img/docImage/232.png)
 
选择Certificates

![图片说明](/img/docImage/233.png)
 
进入下图所示，点击左边的Production，在右边出来的页面的右上角选择添加

![图片说明](/img/docImage/234.png)
 
如图，如果是个人或公司开发证书，选择App Store and Ad Hoc，如果是企业证书，则选择In-House and Ad Hoc，点击Continue进入下一步，在下一页中点击Continue。

![图片说明](/img/docImage/235.png)
 
如图，选择Choose File选择之前生成的certSigningRequest文件，点击Generate

![图片说明](/img/docImage/236.png)
 
如图所示，cer证书创建成功，点击Download将证书下载到本地，然后双击打开证书

![图片说明](/img/docImage/237.png)
 
如图，在钥匙串中找到安装的证书，鼠标点击右键，然后在菜单中选择导出证书，如图：

![图片说明](/img/docImage/238.png)
 
在弹出页面中指定证书名，点击存储，然后输入证书密码，点击好，生成p12格式证书。

![图片说明](/img/docImage/239.png)
 
#**创建App ID**<div id="2"></div>

如图，在左侧菜单选择App IDs，然后点击右上角的添加图标，在接下来的页面里面填写App ID描述，在App ID Suffix栏选择Explicit App ID，在App Services中选择服务功能，如果需要推送功能，则勾选上Push Notifications项，点击Continue进入下一步。
 
![图片说明](/img/docImage/240.png)

![图片说明](/img/docImage/241.png)

![图片说明](/img/docImage/242.png)
 
在新页面中点击Submit，然后点击Done，创建App ID成功。


#**添加测试设备**<div id="3"></div>

个人或公司账号生成的App Store类型mobileprovision证书，应用在没有发布到App Store之前只能在越狱设备上安装，若要在非越狱手机上面安装，则需要把设备添加到Devices里，并且生成Ad Hoc类型mobileprovision证书。

如图选择左侧菜单Devices下面的All，在右侧页面点击右上角添加图标，进入下图所示页面：

![图片说明](/img/docImage/243.png)
 
获取UDID，打开iTunes，连接设备，如图，找到序列号，然后点击序列号，该栏会变成UDID，点击鼠标右键，拷贝UDID。

![图片说明](/img/docImage/244.png)

![图片说明](/img/docImage/245.png)
 
回到网站页面，输入Name和获取的UDID，点击Continue进入下一页，下一页中点击Register，最后点击Done，添加设备完成。

#**云编译mobileprovision证书制作**<div id="4"></div>

##App Store类型证书

如图，点击左侧菜单Distribution，然后点击右侧页面右上角的添加图标，最后选择App Store，点击Continue进入下一步

![图片说明](/img/docImage/246.png)
 
如图，选择App ID，点击Continue进入下一步

![图片说明](/img/docImage/247.png)
 
如图，选择certificates，点击Continue进入下一步

![图片说明](/img/docImage/248.png)
 
输入证书名称，点击Generate，进入下一步完成创建

![图片说明](/img/docImage/249.png)
 
##Ad Hoc类型证书

对于个人和公司账户，Ad Hoc类型证书可以安装到非越狱手机上面调试。如图，选择Ad Hoc，点击Continue进入下一步

![图片说明](/img/docImage/250.png)
 
如图，选择App ID，点击Continue进入下一步

![图片说明](/img/docImage/251.png)
 
如图，选择certificates，点击Continue进入下一步

![图片说明](/img/docImage/252.png)
 
选择设备，然后点击Continue

![图片说明](/img/docImage/253.png)
 
输入证书名称，点击Generate，进入下一步完成创建

![图片说明](/img/docImage/254.png)
 
#**推送证书制作**<div id="5"></div>

在左侧菜单选择Certificates下面的Production，进入到如下界面：

![图片说明](/img/docImage/255.png)
 
点击右上角的添加图标，进入以下页面，选择如图所示内容，点击Continue进入下一步

![图片说明](/img/docImage/256.png)
 
在App ID栏选择对应的AppID，点击Continue，在下一页中点击Continue

![图片说明](/img/docImage/257.png)
 
选择之前生成的certSigningRequest文件，然后点击Generate进入下载界面

![图片说明](/img/docImage/258.png)
 
点击Download下载证书到本地，双击安装到钥匙串中。如下图，在钥匙串中找到此证书，在该证书上面点击鼠标右键，选择导出，然后存储为.p12格式文件，输入证书密码。至此，创建服务端p12格式推送证书完毕。

![图片说明](/img/docImage/259.png)