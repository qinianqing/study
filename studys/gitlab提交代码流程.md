## gitlab提交代码流程

1. 登陆`http://igitlab.chinacloudapp.cn/`，选择New Project

![newproject](newproject.png)

2. Project owner选择diandabrain，Project name自己取，私有项目，创建即可

3. 创建玩之后的页面回又一个简单的介绍，你按照Existing folder or Git repository来做吧（如下）

```shell
cd existing_folder
git init
git remote add origin http://igitlab.chinacloudapp.cn/databrain/<项目名字>.git
git add .
git commit
git push -u origin master
```
4. ​`git commit` 的时候会让你填写commit的的说明（一半会打开一个vi），如果不想写可以直接`git commit -m 'update'`，（这句话是说我提交当前暂存的文件，然后这次提交的说明文字是update）
5. 最后push即可
   1. 如果有新的修改，可以通过`git status`查看当前的修改，然后把需要跟踪的文件加入暂存区（e.g.：`git add foo.html`）,然后`git commit`提交到本地仓库，然后`git push同步到远程仓库

6.版本回退 git reset —hard +版本的ID