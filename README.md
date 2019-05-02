# pylearn
learning while question

#Kivy 是一个开源的 Python 框架，用于快速开发应用，实现各种当前流行的用户界面，比如多点触摸等等。且Kivy 可以运行于 Windows， Linux，MacOS， Android， iOS 等当前绝大部分主流桌面/移动端操作系统。
"""
将Py文件打包成apk文件,江湖上暂有如下3个方法:

1.通过Buildozer;(在linux环境下实现,集成式框架比较容易实现）

2.通过python for android,(这种可以在windows下实现，但需要安装和配置许多内容,较为繁琐)

3.通过Kivy Launcher上打包(需要用到谷歌市场,但想在我大天朝嘛....建议你选择别的)

kivy打包的Buildozer有两种工具，分别是p4a和buildozer。kivydev64使用p4a，kivydev使用buildozer。

buildozer其实是对p4a做了进一步封装，换汤不换药。如果你不想配置recipe和dist之类的参数，可以使用buildozer，但是每次都要复制已经打包成功的项目目录下的.buildozer到要打包的项目目录下，buildozer才不会重复下载sdk和ndk等。而.buildozer目录通常在1G以上，每个项目目录如果都复制一份，不久就会耗尽虚拟机的硬盘空间。所以推荐使用p4a，也就是kivydev64，这个打包环境也是第一个建立在64位ubuntu的环境。
1.安装好环境后，打开VirtualBox,小编遇到的第一个问题就是:
这个问题产生的原因是因为VirtualBox的环境不兼容,win7的话需要将其兼容性配置为Windows Server 2008进行运行;

2. 在成功导入打开的过程中,还会遇到一个问题,会提示你usb接入错误,此时需要你安装这个文件:

3.成功将镜像环境导入后,如果你能看到此神兽Ubantu,说明你的胜利已经在前方:
4. 进入到/home/kivydev//test是测试目录,该目录下的py2apk是py27打包,py3apk是py35打包,这两个版本的差别只在于不同版本的py配置文件,在该目录下的py文件,必须使用main.py命名才能进行打包,先在该目录下对main.py进行编译,看能否成功执行:python3 main.py

5. 可以成功编译后,接下来在py2apk或py3apk的目录下执行打包命令: p4a apk

即可在该目录下产生apk的文件;

6.这里仅作为测试,将该main.py生成的apk进行,在手机上的运行效果如图:

"""

目前，该工具只有一个用于支持Kivy模块的Java bootstrap，开发人员鼓励其他开发者创建出更多的bootstrap。其现在可用的模块包括：peg、pil、png、sdl、sqlite3、pygame、kivy、android、libxml2、libxslt、lxml、ffmpeg、openssl等。

Python for Android以LGPLv2许可证开源，代码托管与Github上。


 #py2exe 测试失败
 """
 pip install py2exe
 
#目标.py文件，即我们需要转换成.exe的文件，命名为test.py
2 print('Hello World!')

 #转换.py文件，即将目标.py文件转换成可单独执行的.py文件,命名为setup.py
2 from distutils.core import setup
3 import py2exe
4 
5 setup(console=['test.py'])


python setup.py py2exe
"""

#pyinstaller 测试成功 poem_opt.py
"""
pip install pyinstaller 即可 在windows下，pyinstaller需要PyWin32的支持。当用pip安装pyinstaller时未找到PyWin32，会自动安装pypiwin32
pyinstaller options myscript.py
pyinstaller --onefile poem_opt.py
-F
-W
pyinstaller -F xxx.py
"""


termux是一款来自国外的终端模拟器，是运行在内部存储上的程序（不在内存卡上），功能比较强大，启动程序之后会进入命令行终端，需要基本的Linux操作知识，众所周知安卓是Linux的阉割版本，所以终端的使用在安卓上也是返璞归真。termux支持apt包管理，所以你可以直接使用：apt－get install ＊＊＊（你要安装的软件包）在线安装软件，当然也支持下载软件包后自行编译安装，debian系统软件deb，可以下载在文件夹后使用dpkg －install 安装，这一部分没有进行验证，但是在termux上是可以进行命令操作的，尽管termux已经实现了很多的linux功能，但是仍然受限于平台，不能与电脑Linux相比。termux的使用与Linux几乎一样，基础功能仍然可以实现。经过我三天的使用探索，已经搭建了我需要的环境，一些学习操作已经可以脱离电脑端，mysql(mariadb),python2,python3,可以运行，ipython启动速度甚至快于Windows命令行的ipython，据说可以在上面运行Java编译器，因为用不到没有验证。甚至如果有需要你可以安装apache2服务器，不过只是部分可行，具体仍然需要后续的验证。值得一提的是Python在termux上运行得很好，有好友需要C和C++的编译器gcc和g++,是完全可以运行的，在搭建环境的时候需要这两个编译器，已经可以安装，不过需要apt－get iinstall clang，这个步骤是必须的。python的安装很简单，方法一，apt－get install python，方法二，pkg install python，这是因为termux有自己维护的适合安卓的软件库，他们在清华大学镜像网站有镜像，如果原来的软件下载安装慢或者不能进行，可以使用清华大学镜像，具体在清华大学镜像网站有步骤。

最近有学习数据库和python所以在安装软件后立即安装这两个软件，mysql和python。但是由于刚刚开始学习和使用出了很多问题。在termux上是不能直接安装mysql的你需要安装他的替代品mariadb，是mysql的一个分支使用的方法一样的:1,pkg install mariadb,2,apt-get install mariadb。安装好以后你就可以使用mysqld来启动你的mysql服务了，启动以后，另外打开一个窗口输入mysql就可以进行使用mysql语句了，和电脑端没有差别，注意手机termux安装mariadb是不需要设置root密码的不过也可以设置，具体后续更新。python的安装相对顺利，直接apt－get install python，当然也要安装pip。不过安装python有些麻烦具体如果有人需要可以给我发邮件dhzzy88@163.com,python库有些无法实现的库不能安装，不过如果你和我一样是初学者，可用的库已经十分丰富了，爬虫scrapy都可以安装了。
启用外置存储

Android6.0以上会弹框确认是否授权,执行这条命令确保termux在最前端(当前Activity)

termux-setup-storage

成功拿到存储权限后会在家目录生成storage目录,并且生成若干目录,软连接都指向外置存储卡的相应目录
高档终端Termux组合了强壮的终端模仿和拓宽Linux包搜集能够使用。

享用bash 和 zsh。

运用nano 和 vim修改文件。

经过ssh拜访服务器。

运用gcc和clang编译代码。

运用python控制台来作为口袋计算器。

运用git 和 subversion查看项目。

运用frotz运转根据文本的游戏

OS苹果用户则可以用这款APP：Pythonista在苹果的应用商店里可以下载到

Termux支持Linux常见的命令，配上黑客键盘这个APP就更加完美了。
$ apt install vim
