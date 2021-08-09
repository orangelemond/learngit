~~~




~~~

~~~
# github或者gitlab用到的用户名和邮箱
$ git config --global user.name "example"
$ git config --global user.email "example@163.com"

# 查看基本配置
git config --list

#key配置
ssh-keygen -t rsa -C "example@163.com"  

#根据提示看.ssh文件存放的路径
- Created directory '/c/Users/liang/.ssh'
# ~/.ssh目录下面会有id_rsa和id_rsa.pub两个文件

cat id_rsa.pub  # 把这个里面的内容复制

#测试是否配置成功
用ssh链接git：ssh -T git@github.com
~~~



项目克隆

~~~
# 克隆项目下来
git clone git@github.com:zhongqiangwu960812/AI-RecommenderSystem.git

# 如果新改了某个文件，需要同步到远程

# 如果是新增了某个文件，可以直接
git add 文件名    
git status  # 可以查看修改情况
git commit -m '新加文件'     # 提交说明
git push    # 提交  

# 如果是删除了某个或者修改了很多地方等，可以
git add .
git commit -m 'update many'
git push

#  如果是从远程仓库改了文件，需要先拉到本地，让本地和远程保持一致之后再push
git pull
~~~



分支

~~~
# 分支的创建与切换， 也可以直接用一行代码：git brance -b 分支名
git branch 分支名
git checkout 分支名

# 修改完了代码，需要push到远程分支上，可以下面操作
git push --set-upstream origin 分支名

# 查看分支
git branch   # 本地分支
git branch -r   # 远程分支
git brance -a  # 查看所有分支
~~~





