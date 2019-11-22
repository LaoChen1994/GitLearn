# Git学习笔记

### 1. git 仓库的常用操作

#### 场景１: 新的仓库本地创建新仓库后推到远端

```bash
# 创建一个新的文件夹
mkdir gitLearn

# 初始化git仓库
git init

# 可以先写一些balabala的文件，　这里用readme代替
cd gitLearn && echo '# GitLearn' >> README.md

# 提交文件
git add .

# commit
git commit -m 'first commit'

# 添加远端仓库
git remote add origin [github仓库地址]

# push
git push origin master

```

#### 场景2.　有远端仓库

+ 直接clone 即可, 如果是走ssh必须在github仓库中配置ssh-key

### 2. 没有冲突的一般git流程

+ git add [所需要提交的文件名]
+ git commit -m [提交需要提示的信息]
+ git push origin [分支名]

### 3. 解决冲突的办法

#### 1. 冲突模拟

+ 用户2和用户1同时修改一个文件
+ 修改完之后一个提交后，另一人提交会出现冲突

1. 先提交用户2的代码到远端

![](/home/cyx/Desktop/Learning/gitLearn/img/选区_013.png)

2. 用户1提交代码到远端

![](/home/cyx/Desktop/Learning/gitLearn/img/选区_014.png)

3. 解决冲突的办法

+ 先通过git pull 拉一下代码, 发现自动合并代码失败, 需要进行手动合并

![](/home/cyx/Desktop/Learning/gitLearn/img/选区_015.png)

+ 打开vscode对需要保留的地方进行更改，这里我们假设两者更改的部分都需要进行修复

![](/home/cyx/Desktop/Learning/gitLearn/img/选区_016.png)

+ 修复完成后我们就解决了冲突， 所有冲突解决完毕之后可以按照正常流程进行提交

### 4. 代码的回滚

[李刚的git撤销回退笔记](https://blog.csdn.net/ligang2585116/article/details/71094887)

#### 1. 模拟代码提交过程

