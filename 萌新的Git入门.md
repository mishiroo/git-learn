[参考资料](https://www.runoob.com/git/git-basic-operations.html)

```
git add README.md  # 把文件添加到暂存区 可传入目录/文件 
# git add .  # 传入所有文件
```



## git的运行结构

![img](https://www.runoob.com/wp-content/uploads/2015/02/git-command.jpg)



## git的创建

```
git init  # 创建该文件夹为一个git仓库
git commit -m "这是提交信息"  # Windows用的是双引号 linux用的单引号
# commit 最好不要传空的
git commit  # 进入vim 可以写的更多

```



## 正确的提交过程

```
git init                           //初始化仓库
git add .(文件name)                //添加文件到本地 
git commit -m “first commit”      //添加文件描述信息

git remote add origin  远程仓库地址 //链接远程仓库 
git remote set-url origin xxxxx.git //修改远程仓库地址

git pull origin main           // 把本地仓库的变化连接到远程仓库master分支
git push -u origin main        //把本地仓库的文件推送到远程仓库master分支
```

==.gitignore==:

比如忽略a/b下的子文件

应写入：**a/b/**,而不是a/b



==pull==字如其名是把网上的代码拔下来到自己本地

==push==字面意思是推，把自己写好的代码推到github上



## 一些重要的命令

```
git remote -v  # 查询远端仓库的地址
```



## 奇怪的知识

Git 中 常常见到origin 为什么使用这个词语?

[(9 封私信 / 80 条消息) Git 里面的 origin 到底代表啥意思? - 知乎 (zhihu.com)](https://www.zhihu.com/question/27712995)

这个名字没有特别的意思，事实上完全可以使用阿猫阿狗进行替换。

和python中的self地位类似，大家约定俗成使用这个代表远端仓库默认名字



**为什么不使用master这个名字了？**

主要因为master有主人的意思，会给人不好的印象 所以2020年10月把master换成main作为默认分支的名字



## 常见bug修复

注意检查自己所在的分支是不是搞混main和master 可能会有超出预期的错误
