# cpp-homeworks-2020
Example project and homework for Cpp
//将远程Github网站上创建并初始化号的仓库，克隆到本地  
git clone [你的Github上仓库的地址链接]  
  
//添加当前仓库中的所有文件,注意add后面有一个空格  
git add .  
  
//本地提交，如果不需要提交到远程仓库，这就成了  
git commit -m "对该版本的描述内容，不可空"  
  
//以下为提交到远程仓库的命令  
//添加远程仓库地址，就是在github上新建的仓库地址链接  
git remote add [自定义一个版本名称如“test”] [对应仓库的网址]  
  
//提交  
git push -u [自定义的版本名称，同上为“test”] master  
  
//之后，输入用户，密码，即可提交，完成后，去github网站上刷新一次就知道了


有时候直接在github网站上修改了，本地没有修改再push新的会报错

这时要么把远程的pull下来，合并到本地文件中

要么把本地舍弃，直接把远程的pull下来


以下是举例：



You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you can merge.


错误可能是因为在你以前pull下来的代码没有自动合并导致的.

有2个解决办法:

1.保留你本地的修改

git merge --abort

git reset --merge

合并后记得一定要提交这个本地的合并

然后在获取线上仓库

git pull


2.down下线上代码版本,抛弃本地的修改

不建议这样做,但是如果你本地修改不大,或者自己有一份备份留存,可以直接用线上最新版本覆盖到本地

git fetch --all

git reset --hard origin/master

git fetch

9.16
git init 
创建git.文件夹

