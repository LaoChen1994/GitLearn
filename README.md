# GitLearn

### git 仓库的常用操作

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
