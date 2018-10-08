## 环境
需要的环境包括node.js, npm 以及 @angular/cli

1. 首先，到官网 https://nodejs.org/zh-cn/ 下载Node.js 安装包。
	(如果被墙，可以选择中文站点 http://nodejs.cn/download/ 进行下载)。目前可以选择（8.9.1 LTS 推荐）版本。下载后运行。
	在Windows上安装时务必选择全部组件，包括勾选Add to Path。

	安装好以后，系统中应该已经包括了node.js与npm系统。
	用以下命令来验证是否安装好：
	C:\Users\yanglg>node -v
	v8.9.0

	C:\Users\yanglg>npm -v
	5.5.1

	出现类似以上信息时，说明 node.js 与 npm 已经安装好了。
	
2. 安装  @angular/cli
	npm i -g @angular/cli

	如果被墙或者遇到麻烦，可以使用国内的淘宝源看看：
	npm config set registry https://registry.npm.taobao.org
	npm i -g @angular/cli

	或者直接改用cnpm试试看：
	npm i -g cnpm
	cnpm i -g @angular/cli

3. 为环境安装模块
	从命令行进入进入项目根目录，执行以下命令：
	npm install

	如果安装过程中被墙或者遇到其他麻烦，可以使用国内的淘宝源看看：
	npm config set registry https://registry.npm.taobao.org
	npm install

	或者直接改用cnpm试试看：
	npm i -g cnpm
	cnpm install
	

## 编译打包
从命令行进入进入项目根目录，依次执行以下命令：(环境已经被安装好的情况下)

	ng build --prod
	
	如果过程顺利，将在本项目根目录中生成 dist 子目录，即为编译打包的目标文件夹。把它拷贝部署到实际的 web 服务器相应的工作目录即可。


## 调试注意事项
	.angular-cli.json 文件中
	apps.assets 数组中增加 一项数据 【,"mock"】 才能获得 mock 数据。(angular5的新要求)，在打包的时候，注意把该项数据去掉。

	调试命令：	 
	ng serve

打开你的浏览器，访问http://localhost:4200/

如果你想让加载的包更小，请使用以下方式启动angular-cli内置的轻量级http server

	ng serve --prod
  
 ## 该实例为打包后的项目，如有需把该项目拷贝部署到实际的 web 服务器相应的工作目录即可。


![image](https://github.com/MadmanLiang/WebAdmin/blob/master/demo.gif?raw=true)
