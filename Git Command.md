### Git用法记录篇:pig::pig:

anyway, start from 2022/07, hope to be better:smiling_imp::smiling_imp:

First of all, need to install git. pls follow guide from google or Baidu to install it, easy installation.  
首先选个做测试的目录，在E盘：E:\Git_repository\test  
![image](https://user-images.githubusercontent.com/32427537/179387818-ed8555a8-c8d6-4bc5-af48-1a667f29a7e8.png)

#### 1.基本操作  
右键，Git Bash Here,既有窗口弹出  
git status  
git init  
![image](https://user-images.githubusercontent.com/32427537/179390780-641f4601-a15c-41c2-8dc9-d79e0ccf46da.png)

git add  
![image](https://user-images.githubusercontent.com/32427537/179390694-ea9ad78f-2345-452a-8fcc-8afef12b10e8.png)  

git commit  
git log  
git branch  
git checkout  
git merge  
git branch -d or git branch -D  
git tag  

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
可以看到已经有 SSH 了。接下来，输入command `ssh-keygen -t rsa`，表示我们指定 RSA 算法生成密钥，然后敲三次回车键，期间不需要输入密码，之后就就会生成两个文件，分别为id_rsa和id_rsa.pub，即密钥id_rsa和公钥id_rsa.pub.   
对于这两个文件，其都为隐藏文件，默认生成在以下目录：Linux 系统：~/.ssh  
Mac 系统：~/.ssh  
Windows 系统：C:\Documents and Settings\username\\.ssh  
Windows 10 ThinkPad：C:\Users\think\.ssh密钥和公钥生成之后，我们要做的事情就是把公钥id_rsa.pub的内容添加到 GitHub，这样我们本地的密钥id_rsa和 GitHub 上的公钥id_rsa.pub才可以进行匹配，授权成功后，就可以向 GitHub 提交代码啦！

##### 2.2 

