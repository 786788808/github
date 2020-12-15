### 一. 背景：  
突然，发现！github显示不了头像，文章里的图片也显示不出来。想着是内网网速问题，就没管了。  
但是，过了几天，翻墙网速也不佳，连网页都进不去……    
于是，我发现，这是个问题，需要解决一下。   
![](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1197072620,3809781488&fm=26&gp=0.jpg)
>
### 二. 解决步骤：  
#### (2.1) 按路径打开C:\Windows\System32\drivers\etc,找到hosts  
#### (2.2) 右击属性，安全，编辑，勾选允许写入。经过上一步，可以在hosts写入新东西了。      
![](https://ftp.bmp.ovh/imgs/2020/12/aa35b7b11bc99ace.png)
#### (2.3) 双击hosts，打开来修改。我用pycharm编辑器编辑，大家按照各自习惯选择即可。  
在hosts的最后，复制下列设置并保存即可。      
```
# GitHub Start
192.30.253.112    Build software better, together
192.30.253.119    gist.github.com
151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
151.101.184.133    avatars0.githubusercontent.com
151.101.184.133    avatars1.githubusercontent.com
151.101.184.133    avatars2.githubusercontent.com
151.101.184.133    avatars3.githubusercontent.com
151.101.184.133    avatars4.githubusercontent.com
151.101.184.133    avatars5.githubusercontent.com
151.101.184.133    avatars6.githubusercontent.com
151.101.184.133    avatars7.githubusercontent.com
151.101.184.133    avatars8.githubusercontent.com

 # GitHub End
 ```
 看图片：  
 ![](https://ftp.bmp.ovh/imgs/2020/12/576bdadb2cbb03eb.png)  
 保存之后，刷新github即可。  
![](https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3728565027,38407514&fm=26&gp=0.jpg)
 
