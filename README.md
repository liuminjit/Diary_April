# Diary_April

## Diary 【4.1】

### gihub使用

1. mkdir + 空格  + 文件夹名 ——创建文件夹
2. cd + 空格 + 文件夹名 + /（正斜杠）  ——进入文件夹
3. git clone https://github .......... .git  —— 克隆项目到本地
4. 
## Diary 【4.11】
### 在Github Pages搭建自己写的页面
准备工作：

1. 需要你自己写的网页文件
2. 注册Github
3. 下载安装git

教程开始：

1. 步骤一：登录到Github上，新建一个repo，命名为test，勾选 initialize this repository with a README，点击create repository
2. 步骤二：打开settings，有一个Github Pages 的设置，点击 source 中的本来的 None ，使其变成 master 分支，也就是作为部署github pages 的分支，然后点击 save
3. 步骤三：页面刷新之后，再看 github pages 设置框处，多了一行网址，就是你的 github pages 的网址了,点击这个链接,就可以发现已经创建成功
4. 步骤四 ：打开此电脑，选择一个盘，比如 f 盘，右键空白处点击 git bash here
5. 步骤五：输入如下命令，用来在 f 盘创建 test 文件放你的github上的test repository，克隆test repository到 test 文件中。(命令是mkdir + 空格 + 文件名 ，进入刚刚的文件夹  cd + 空格 + 文件名 + / ，接下来git clone https:// 克隆项目到本地)
6. 步骤六： 将自己的网页文件复制粘贴至 f 盘的 test 文件中
7. 首先输入  git status   列出当前目录所有还没有被git管理的文件和被git管理且被修改但还未提交(git commit)的文件，也就是所有改动文件，红色字体标出。然后输入 git add .  (有个点) 表示添加当前目录下的所有文件和子目录，然后 再输入一次 git status 如果看见文件都变绿了 ，那么就代表 它们已经准备好了被提交（git commit）。
8. 步骤九：输入如下命令，将你的文件上传至远程 master 分支 git commit -m "modify" 提交修改为modify  再git pull 拉取一次 看看是否已经是最新的了
9. 输入最后一行 git push，按回车，等一会，会有弹出框让你输入你的 github 账号和密码。
10. 打开浏览器输入给你的网址加上你上传的 html 文件名 test.html，然后重重的按下回车

附录一：常用git命令：

$ git clone  //本地如果无远程代码，先做这步，不然就忽略

$ cd //定位到你blog的目录下

$ git status //查看本地自己修改了多少文件

$ git add . //添加远程不存在的git文件

$ git commit  -m "what I want told to someone" //提交修改

$ git push  //更新到远程服务器上

$ git rm //移除文件
