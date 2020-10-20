## 安装git
1. 打开并选择自己系统对应的去下载(git安装地址)[https://git-scm.com/downloads]
2. 下载完毕后进行安装（安装到任意盘）
3. 检查是否安装成功：
```
$ git --version（查看版本号）
```


## 注册GitHub账号


1. (打开GitHub地址)[https://github.com/]进行注册，输入有效的邮箱（后期会在邮箱中进行验证），输入用户```````名（最好是英文），输入密码，点击注册按钮，会发送给邮箱一个验证，打开邮箱进行验证；
2. 注册成功后进行登陆；
3. 打开终端输入以下命令
```
$ ssh-keygen -t rsa -C "your_email@example.com"(邮箱填注册GitHub的邮箱地址)
```
4. 在本地C盘的用户文件夹下的各个文件夹去找（下载、桌面、音乐等程序）存在的目录，找到同级目录下的.ssh文件`````夹，打开后复制.pub后缀的文件内容；
5. 打开GitHub的设置下的ssh and GPG keys点击new ssh key按钮，将复制的内容粘贴到key字段下的文本域中，然`````后点击Add SSH key；
6. 打开终端执行以下命令：
```
$ git config --global user.email 'GitHub的邮箱名'
$ git config --global user.user 'GitHub用户名'
```

## 提交代码到GitHub账号上
1. 在GitHub新建仓库
2. 复制仓库ssh地址在本地想要保存的路径打开git bash 并执行 $ git clone 仓库代码地址
3. 然后在克隆下来的文件夹里放入自己想要提交的代码
4. 执行以下命令
```
$ git init (初始化git环境)
$ git add . （添加要提交的代码）
$ git commit -m '提交信息' （添加提交信息说明） 
$ git remote add origin git@github.com:benben0513/newFile.git （从当前的 github 下的新创建的仓库 找 类似 的 git remote ）
$ git branch -M main （在本地新建一个main分支）;          (二选一)
$ git checkout -b zhangwenxiao (zhangwenxiao 分支名);    (二选一)
$ git pull origin main (拉取远程最新代码)
$ git push origin main （提交本地代码到GitHub仓库）
```
5. 刷新并查看GitHub上本次提交的代码



## 加入一个github仓库 步骤
1. 克隆仓库
$ git clone 仓库地址(ssh 要克隆的仓库地址)

2. 进入本地仓库文件夹创建分支
$ cd 文件夹名称
$ git checkout -b 分支名(和创建仓库的分支名保持一致)

3. 提交代码
$ get add .
$ git commit -m '提交信息'
$ git push origin 本地分支名