# pylearn
learning while question

#Kivy 是一个开源的 Python 框架，用于快速开发应用，实现各种当前流行的用户界面，比如多点触摸等等。且Kivy 可以运行于 Windows， Linux，MacOS， Android， iOS 等当前绝大部分主流桌面/移动端操作系统。
"""

"""

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
"""
