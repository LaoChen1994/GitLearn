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

	+ 在两个不同文件夹中拷贝测试的git仓库
	+ 同时修改一个文件并先后提交

1. 先提交用户2的代码到远端

![](/home/cyx/Desktop/Learning/gitLearn/img/选区_013.png)



