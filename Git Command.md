### Git用法记录篇:pig::pig:

anyway, start from 2022/07, hope to be better:smiling_imp::smiling_imp:  

收集的资料：  
- 中文版介绍git的书，看书名就很Pro:[Pro Git book](https://git-scm.com/book/zh/v2)

First of all, need to install git. pls follow guide from google or Baidu to install it, easy installation.  
首先选个做测试的目录，在E盘：E:\Git_repository\test  
![image](https://user-images.githubusercontent.com/32427537/179387818-ed8555a8-c8d6-4bc5-af48-1a667f29a7e8.png)

#### 1.基本操作  
右键，Git Bash Here,既有窗口弹出  

+ **配置用户名和邮件地址**  
如果有用--global选项，那么该command只需要执行一次   
`git config --global user.name "Hush"`  
`git config --global user.email hushemail@example.com`    

+ **查看配置信息**  
`git config --list`

+ **git status**  
查看仓库的状态,这里的信息提示很友好，如果你忘了在整个提交代码过程中到了哪一步，no worry, just use `git status`to help you.  

+ **git init**  
![image](https://user-images.githubusercontent.com/32427537/179390780-641f4601-a15c-41c2-8dc9-d79e0ccf46da.png)

+ **git add**  
![image](https://user-images.githubusercontent.com/32427537/179390694-ea9ad78f-2345-452a-8fcc-8afef12b10e8.png)  

+ **git commit**  
+ **git log**  
`git log`可以看到谁提交过什么  
`git log -2`,可以最近的两次提交  
`git log -p`,显示每次提交所引入的差异  

+ **git branch**  
git branch -d or git branch -D  

+ **git checkout**  
+ **git merge**   
+ **git tag**  

#### 2.实现通过 Git 向 Github 提交代码 
anywany, git 还是 git， Github 还是 Github, 好像还没联动起来。 现在我们就去让他们联谊。  
涉及到 SSH 相关知识……
（ssh全称“Secure Shell”，指的是“安全外壳协议”，是专为远程登录会话和其他网络服务提供安全性的一种协议；利用SSH协议可以有效防止远程管理过程中的信息泄露问题，弥补网络中的漏洞。）  
Git是分布式的代码管理工具，远程的代码管理是基于SSH的，所以要使用远程的Git则需要SSH的配置。  
##### 2.1 生成 SSH key
首先要确保已经安装了 SSH。
我们要想生成SSH key，首先就得先安装 SSH，对于 Linux 和 Mac 系统，其默认是安装 SSH 的，而对于 Windows 系统，其默认是不安装 SSH 的，不过由于我们安装了 Git Bash，其也应该自带了 SSH.  
可以通过在 Git Bash 中输入ssh命令，查看本机是否安装 SSH：  
![image](https://user-images.githubusercontent.com/32427537/179390020-1851a05a-fee5-479c-ae21-527acd97532b.png)  
可以看到已经有 SSH 了。接下来，输入command `ssh-keygen -t rsa`，表示我们指定 RSA 算法生成密钥，然后敲三次回车键，期间不需要输入密码，之后就就会生成两个文件，分别为 id_rsa 和 id_rsa.pub，即密钥 id_rsa 和公钥 id_rsa.pub.   
位置在命令行界面输出，照着进去就行了。(Mine: /c/Users/Administrator/.ssh/id_rsa )
接下来，把公钥 id_rsa.pub 加到 GitHub，让本地的密钥 id_rsa 和 GitHub 上的公钥id_rsa.pub 匹配

##### 2.2 种 key
![image](https://user-images.githubusercontent.com/32427537/179391688-0c6110f2-9682-4e86-b4b8-4760f483b78e.png)![image](https://user-images.githubusercontent.com/32427537/179391763-3f358349-c17a-429e-b8c6-ebd0c0f82803.png)
![image](https://user-images.githubusercontent.com/32427537/179391919-cdbc943e-2a9b-4941-9054-7e03e56bd222.png)  
![image](https://user-images.githubusercontent.com/32427537/179391851-ddf5bd32-d6a8-4aeb-bc81-5afdb1ecc32a.png)
 
##### 2.3 验证是否种key成功
种完key，我的邮箱收到确认信息。and then, 用命令来试试水,`ssh -T git@github.com`    
![image](https://user-images.githubusercontent.com/32427537/179392141-a2598029-d125-4e83-bcbd-a77d610f63de.png)  
此结果告诉我们Git与Github已经绑定啦  
种key完毕，恭喜恭喜:bowtie::bowtie:  

#### 3.实操：通过 Git 向 Github 提交代码
讲甘多，终于可以到实操环节:punch:  

进入github，找到相关项目，然后点进去，`code`,复制URL，然后回到local, 找个位置放code。比如我想在这里放code，E:\Git_repository\test20220731\for_Amazon， 在当前目录，右击，jit bash here。  
![image](https://user-images.githubusercontent.com/32427537/182013268-a8eefeda-a0ac-4f2a-9cff-0fbfb1a0a1a1.png)  
在终端输入， `git clone xxxx_URL`  
![image](https://user-images.githubusercontent.com/32427537/182013373-3e82bf62-bdfd-4c0e-93b9-5459f5d6883b.png)  
这样就可以把项目的所有东西克隆到本地了，可以自行验证一下。    

实验一拨，现在在目录下新建两个文件夹
`cat ~/.gitconfig`, 可以查看git的配置文件  





待补，加班先20220717
疯狂的周末 困




