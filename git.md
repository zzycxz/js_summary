## git 介绍
### 一、版本控制
- 1、我们的代码也需要备份，修改完成之后提交给保本库进行保管，记录每一个版本，供还原，穿越。
- 2、多端共享，可以在多端进行共享
- 3、团队写作，多个人或团队合作编写一个项目 **解决冲突**，手动或者自动
- 4、git拥有强大的分支管理系统

### 二、什么是git
- linus花了两周时间自己用c写了一个分布式版本控制系统，就是git。

### 三、分布式
- svn(集中式) 需要有一台中央服务器
- git(分布式) 更安全
- git速度比svn更快
- svn中每个文件中都有一个文件.svn文件，git 有一个单独的文件夹 .git文件夹

### 四、区域
- 工作区
- 暂存区/过渡区
- 历史区/版本库

## git使用
### 一、安装
- windows
- mac 如果安装过xcode自带git，homebrew mac的包管理 (ohmyz.sh) 安装插件 iterm2

## 二、配置用户(不配置不能提交代码)
```
git config --list
git config --global user.name "yourname"
git config --global user.email “youremail”
```

### 三、初始化git
- 不要在文件夹里初始化，一个项目初始化一次，不能嵌套着来
```
git init 告诉git哪个文件夹被git所管理
git status 查看git状态
```
### 四、删除暂存区
```
git rm --cached . -r 递归形式删除暂存区
```
### 五、添加到暂存区
```
git add ./ -A / 文件名
```
### 六、提交历史区
```
git commit -m "消息" 提交到历史区，必须后跟着信息

git log 得到提交的版本号，作者，日期
```
### 七、git的对比
- git diff 工作区和暂存区
- git diff 分之名 工作区和历史区
- git diff --catched 暂存区和历史区比较

### 八、暂存区回滚操作
- 从暂存区中将工作区内容覆盖掉
```
git checkout 文件名  暂存区中将工作区内容覆盖掉

git reset HEAD 文件名 / 。  暂存区网上回滚一次
```

### 历史区回滚找版本号
```
git log 得到版本号

git reset --hard 版本号  直接把工作区和暂存区回滚到版本号版本

git reflog 打出所有的日志 用此命令找到所有版本号，包括回滚回去后的时间点之后的

然后重新git reset --hard 版本号

git reset --haed HEAD^ 回到上一个版本
```
## 另附：基础linux命令
- pwd print working directory
- rm -rf ‘文件名’ 所有的文件夹中的递归 贼好用，建议加*
- rm 文件名 删除
- mkdir 文件夹名 创建目录
- cd 目录名 change directory
- ls -al 显示目录下所有的文件和权限
- touch 文件名 创建文件
- cat 文件名 显示文件内容
- vi 文件名 i插入模式 esc 退出编辑模式 :q!强制推出  :wq! 保存并退出
