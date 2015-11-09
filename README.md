<h4>准备</h4>
<ol>
	<li>确保你的电脑显卡支持OpenGL，如果没有，请将显卡驱动更新到最新版本。</li>
	<li>访问 Github 托管库 <a href="https://github.com/haozzzzzzzz/osgEarthX-binary" target="_blank">osgEarthX-binary</a>，将最新的可执行程序下载或者同步到本地。</li>
	<li>将下载的压缩包解压到磁盘的任意目录下，例如我存放在“E:\OpenSceneGraph\osgEarthX-binary\”。</li>
</ol>
<h4>配置环境变量</h4>
<ol>
	<li>在“我的电脑”图标中点击鼠标右键查看系统“属性”，在系统属性窗体左侧点击“高级系统设置”，在系统属性对话框中点击“环境变量”按钮弹出环境变量设置对话框。
<a href="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109011240059.png?1366x768_130" target="_blank"><img src="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109011240059.png?1366x768_130" alt="设置系统环境变量" width="1366" height="768" /></a> 设置系统环境变量</li>
	<li>点击“系统变量”中“新建”按钮，新建一个“变量名”为“OSG_DIR”（不包含双引号，下同）的变量，“变量值”为osgEarthX可执行程序所在的目录，例如“E:\OpenSceneGraph\osgEarthX-binary\”，点击“确定”按钮完成添加。

<a href="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109012922092.png?409x188_130" target="_blank"><img src="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109012922092.png?409x188_130" alt="编辑系统变量" width="409" height="188" /></a> 编辑系统变量</li>
	<li>与步骤2同样，新建一个“变量名”为“OSG_BIN_DIR”的变量，值为“;%OSG_DIR%\bin;”（分号为英文分号，下同）。</li>
	<li>新建一个“变量名”为“OSG_FILE_PATH”的变量，值为“;%OSG_DIR%\data;%OSG_DIR%\tests;”。</li>
	<li>选中“PATH”变量进行编辑，在值编辑框的最后添加“;%OSG_BIN_DIR%;”。</li>
	<li>（可选）新建一个“变量名”为“OSG_WINDOW”的变量，值为“100 100 1000 600”。此变量用来设置OSG程序已窗体的形式显示，如果不设，则默认为全屏显示。</li>
	<li>（可选）新建一个“变量名”为“OSG_VER”的变量，值为“3.2.1”。</li>
	<li>点击“确定”完成对环境变量的设置。</li>
</ol>
<h4>测试 osgEarthX 环境</h4>
完成以上的准备和设置后，运行CMD，分别输入以下命令：
<ol>
	<li>osgviewer</li>
	<li>osgviewer boxman.osg</li>
	<li>osgearth_viewer</li>
	<li>osgearth_viewer gdal_tiff.earth</li>
</ol>
如果以上命令都能被执行，并显示出正确的信息，那么说明 osgEarthX 的环境基本上已经完成。

<a href="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109013653089.png?1366x768_130" target="_blank"><img src="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109013653089.png?1366x768_130" alt="osgearth_viewer gdal_tiff.earth" width="1366" height="768" /></a> 
osgearth_viewer gdal_tiff.earth

<h4>注册 osgEarthX_COM 组件</h4>
<ol>
	<li>找到 osgEarthX 可执行文件目录 bin 目录下的 osgEarthX_COM.dll 文件的绝对路径，例如我的是“E:\OpenSceneGraph\osgEarthX-binary\bin\osgEarthX_COM.dll”。</li>
	<li>以管理员身份运行CMD，运行注册命令regsvr32加上你找到的osgEarthX_COM.dll的绝对路径，例如“regsvr32 E:\OpenSceneGraph\osgEarthX-binary\bin\osgEarthX_COM.dll”。如果注册成功则会弹出“注册成功”的提示对话框。</li>
	<li>如果要卸载该组件，可运行“regsvr32 \u ”加上你的绝对路径，例如“regsvr32 \u E:\OpenSceneGraph\osgEarthX-binary\bin\osgEarthX_COM.dll”。</li>
	<li>如果注册成功，可点击osgEarthX可执行程序目录下demo目录下的Demo_WinForm.bat运行示例，如果一切正常，将会显示如下程序。

<a href="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109014119017.png?296x298_130" target="_blank"><img src="http://img17.poco.cn/mypoco/myphoto/20151109/01/17843243820151109014119017.png?296x298_130" alt="test_CSharp" width="296" height="298" /></a> test_CSharp</li>
</ol>
<h4>更多阅读</h4>
<ul>
	<li>去 <a href="http://osgearth.org/" target="_blank">osgearth.org</a> 查看 osgEarth 原有的用法和文档。</li>
</ul>
