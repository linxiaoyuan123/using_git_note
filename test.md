git和github基本用法

1.wd
显示当前终端所在的会话位置

2.ls
显示当前目录下的所有文件

3.cd
切换路径

4.git version
git版本号

5.git config --global user.name "用户名"
设置用户名

6.git config --global user.email "邮箱"
设置邮箱

7.git add test.txt
添加文件到暂存区

8.git commit
会进入vim编辑器，输入a或者i进入编辑模式，然后输入注释，按esc键退出编辑模式，输入:wq保存并退出

9.git commit -m "注释"
将暂存区文件提交到本地仓库

10.提交文件说明要规范
ep:git commit -m "fix(test):change content"
fix修复（修复的文件或模块）:"修改的内容"

11.VSCODE有自带的界面版git操作
步骤：点源代码管理->可以看到暂存区和已修改文件->点左上角的确认按钮->点提交->输入提交信息

VSCODE自带git的所有基本操作，高级功能可以安装一个git history diff插件

具体其他功能查菜鸟

12.若想回退某个版本，则git log，复制那个版本的commit的id
git reset --hard 版本id(右键复制)

13.若想在不同版本中切换，可以用创建分支（分支就是将当前版本复制一份）————>主要用于团队协作
创建分支：
git branch 分支名
切换分支：
git checkout 分支名
合并分支：
git merge 分支名
删除分支：
git branch -d 分支名

团队协作举例：项目主分支版本为1.0，1.1版本要添加5个新功能，将5个功能分配给5个人，
这5个人在1.0版本的基础上branch出去一个自己的版本，分支名为功能xxxx
完成后，在主分支把5个人的5个分支都merge过来合并一起，再提交并使用git tag（tag命令创建固定版本）打标签生成1.1版本

git的团队协作需要一个服务器，搭建一个git仓库服（服务器仓库），例如gitlab，Bitbucket

一般人用github或gitee这种公共云服务器仓库(类比符合git操作的网盘)

14.git init
初始化仓库，在当前目录下创建一个.git隐藏文件，这个文件就是仓库文件




