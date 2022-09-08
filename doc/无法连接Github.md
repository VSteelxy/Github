# Github500 无法显示问题
```
- 养成习惯：git操作之前先将远程仓库拉取到本地，一定要保持本地版本不能低于远程
- 因为我没有下载markdown，所以编写md文件习惯在GitHub编写可以边编写边看效果，导致远程仓库的版本一直高于本地
```
> 个人想法
- 背景：Github的服务器在漂亮国，我们平时登录Github会发现非常的慢，经常就是连接不上；因此成为了我向大佬学习的绊脚石&#x1f606;
- 原因：Github中的所有域名需要转换成ip；首先会查找本地hosts文件；没有会往上级DNS服务器查询，层层递进
- 思路：无法显示问题有很多因素，本文的域名缓存只是一个加速连接的手段，通过直接在本地的DNS服务器中记录对应的域名解析减少向上查询的时间

> 省流步骤
- 步骤零：hosts文件的路径（Windows系统）是```C:\windows\system32\drivers\etc\hosts```；修改hosts文件需要管理员权限
- 步骤一：home+Q打开搜索界面；搜索cmd用管理员身份打开cmd
- 步骤二：记事本打开hosts文件```notepad C:\windows\system32\drivers\etc\hosts```
- 步骤三：填写域名对应的ip（在文件最后填写下面的代码）
```
# GitHub520 Host Start 

185.199.108.154 github.githubassets.com 
140.82.114.21 central.github.com 
185.199.108.133 desktop.githubusercontent.com 
185.199.108.153 assets-cdn.github.com 
185.199.108.133 camo.githubusercontent.com 
185.199.108.133 github.map.fastly.net 
199.232.69.194 github.global.ssl.fastly.net 
140.82.113.4 gist.github.com 
185.199.108.153 github.io 
140.82.114.3 github.com 
140.82.113.5 api.github.com 
185.199.108.133 raw.githubusercontent.com 
185.199.108.133 user-images.githubusercontent.com 
185.199.108.133 favicons.githubusercontent.com 
185.199.108.133 avatars5.githubusercontent.com 
185.199.108.133 avatars4.githubusercontent.com 
185.199.108.133 avatars3.githubusercontent.com 
185.199.108.133 avatars2.githubusercontent.com 
185.199.108.133 avatars1.githubusercontent.com 
185.199.108.133 avatars0.githubusercontent.com 
185.199.108.133 avatars.githubusercontent.com 
140.82.113.10 codeload.github.com 
52.216.226.40 github-cloud.s3.amazonaws.com 
52.216.162.99 github-com.s3.amazonaws.com 
52.216.142.196 github-production-release-asset-2e65be.s3.amazonaws.com 
52.217.97.236 github-production-user-asset-6210df.s3.amazonaws.com 
52.217.194.41 github-production-repository-file-5c1aeb.s3.amazonaws.com 
185.199.108.153 githubstatus.com 
64.71.168.201 github.community 
185.199.108.133 media.githubusercontent.com 

# GitHub520 Host End
```
> 总结
- 保存域名ip对应关系只是一种加速的手段，效果不是很明显
