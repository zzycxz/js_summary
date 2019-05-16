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
