# WAMP初探

 1. 修改默认启动的浏览器
 2. 修改默认www根目录映射
 3. 修改wapm控制面板www根目录


----------
wamp版本：WampServer Version 3.0.6 32bit

## 修改默认启动浏览器 ##
 

 - 找到wamp所在安装目录
 - 找到 wampmanager.conf （有三个wampmanager文件，注意是 .conf结尾那个）。打开该文件 “ctrl + F” 查找 “navigator”。将你想要默认监听的浏览器启动路径替换。![此处输入图片的描述][1]
 ![此处输入图片的描述][2]
 - 重启wamp服务

## 修改默认www根目录映射 ##
&nbsp;&nbsp;&nbsp;&nbsp;在wamp 鼠标左键控制面板中有一栏“www目录”选项，我们把项目文件扔到该目录下，apache就能监听我们的项目文件。然而在实际项目中 “www”这个文件夹在系统安装的 wamp 目录下， 对于我们的项目开发文件位置总有一些不方便，为此我们想将映射文件夹自定义改为我们计算机中的某个文件夹。我们可以这样做：

 - 控制面板找到 Apache > httpd.conf
 ![此处输入图片的描述][3]
 - "ctrl + F" 搜索分别找到 “DocumentRoot” 和 “Directory” , 将你要自定义监听的路径作修改（我这里改为 F:/phpstudy）
 ![此处输入图片的描述][4]
![此处输入图片的描述][5]
 - 控制面板找到 Apache > httpd-vhosts.conf 。 里面的DocmentRoot和Dorectory 下的监听路径也要修改（版本3.0以上，2.0+稍有不同，不用在这个修改就可以生效）
![此处输入图片的描述][6]
 - 重启wamp, 项目文件夹映射成功
## 修改wapm控制面板www根目录 ##
&nbsp;&nbsp;&nbsp;&nbsp;我们成功地修改服务器监听的 项目文件夹路径。但我们还想修改wamp控制面板中 www目录栏点击后能打开到我所自定义监听的文件路径中去，我们可以这样做：
 - 找到 “wampmanager.ini” , “wampmanager.tpl”文件
![此处输入图片的描述][7]
 - 分别“ctrl + F” 搜索找到 “Menu.Left”,做如下修改 
![此处输入图片的描述][8]
![此处输入图片的描述][9]
 - 重启wamp
 
 
  
 


  [1]: https://github.com/hedonghui/article/blob/master/php/screenshot/php1.jpg
  [2]: https://github.com/hedonghui/article/blob/master/php/screenshot/php2.jpg
  [3]: https://github.com/hedonghui/article/blob/master/php/screenshot/php3.jpg
  [4]: https://github.com/hedonghui/article/blob/master/php/screenshot/php4.jpg
  [5]: https://github.com/hedonghui/article/blob/master/php/screenshot/php5.jpg
  [6]: https://github.com/hedonghui/article/blob/master/php/screenshot/php7.jpg
  [7]: https://github.com/hedonghui/article/blob/master/php/screenshot/php8.jpg
  [8]: https://github.com/hedonghui/article/blob/master/php/screenshot/php9.jpg
  [9]: https://github.com/hedonghui/article/blob/master/php/screenshot/php10.jpg