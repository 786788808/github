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
可以看到已经有 SSH 了。接下来，输入command `ssh-keygen -t rsa`，表示我们指定 RSA 算法生成密钥，然后敲三次回车键，期间不需要输入密码，之后就就会生成两个文件，分别为 id_rsa 和 id_rsa.pub，即密钥 id_rsa 和公钥 id_rsa.pub.   
位置在命令行界面输出，照着进去就行了。(Mine: /c/Users/Administrator/.ssh/id_rsa )
接下来，把公钥 id_rsa.pub 加到 GitHub，让本地的密钥 id_rsa 和 GitHub 上的公钥id_rsa.pub 匹配

##### 2.2 种 key
![image](https://user-images.githubusercontent.com/32427537/179391688-0c6110f2-9682-4e86-b4b8-4760f483b78e.png)   
![image](https://user-images.githubusercontent.com/32427537/179391763-3f358349-c17a-429e-b8c6-ebd0c0f82803.png)   
![image](https://user-images.githubusercontent.com/32427537/179391783-23094f6e-023f-433d-8ca4-6171c8df8cf9.png)   
![image](https://user-images.githubusercontent.com/32427537/179391851-ddf5bd32-d6a8-4aeb-bc81-5afdb1ecc32a.png)
 



