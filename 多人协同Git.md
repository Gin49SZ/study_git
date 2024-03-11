# 多人协作

如何实现多人协作，共同开发一个项目，每个人负责一些功能？

**为每个人创建一个dev分支，或者以每个人负责的功能为命名创建dev分支（git/flow工作流）**

![多人协作开发流程](多人协作开发流程.png)

## 在github中添加合作者

### 1.个人添加

在仓库的settings选项中，选择collaborators选项

![添加合作者](添加合作者.png)

### 2.组织添加

创建一个组织

![创建组织](创建组织.png)

设置组织的一系列信息后即可创建完毕，无需邀请其他成员，直接继续即可进入组织界面

![组织界面](组织界面.png)

新建一个组织项目dbhot，然后推送第一个版本

![dbhot for org](dbhot for org.png)

版本名称应该是v1.0之类而不是具体的描述，如何添加对应的版本号？

使用`git tag`**添加Tag**

```
$ git tag -a v1 -m "第一版"

$ git log
commit b933935d4bf99eb8a665fb36b1a88e924ae756a9 (HEAD -> master, tag: v1, origin/master)
Author: Gin49SZ <1003690614@qq.com>
Date:   Mon Mar 11 18:12:56 2024 +0800

    东北热基本功能

```

将tags推到远程仓库

```
$ git push origin --tags 
```

通过点击`tag`即可查看对应的版本

![tag标签](tag标签.png)

可以通过点击`tags`可以查看标签和release版本

![点击tag](点击tag.png)
