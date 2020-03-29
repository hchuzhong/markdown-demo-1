# 如何用 Hugo 搭建个人博客

## 1.安装 Hugo

 Hugo 的官方安装教程为：[Hugo 官方安装教程](https://gohugo.io/getting-started/installing)

或者可以按照以下教程：

### Mac 安装方式

在终端依此运行以下两行命令，运行第二行命令后出现 Hugo 的版本号，证明安装完成

```
    brew install hugo
    hugo version
```
### Windows 安装方式

1. 前往 [Hugo releases](https://github.com/gohugoio/hugo/releases) 按照当前你所用系统的版本下载对应的 Windows 版本的 Hugo ，有 64 位和 32 位两种
2. 解压，将 hugo.exe 放到你平时放置软件的盘中，再将 hugo.exe 当前所在的路径添加到 PATH 中，PATH 打开的方式为：此电脑 -> 右键属性 -> 高级系统设置 -> 环境变量 -> PATH 
3. 重启或打开你所使用的终端，输入 hugo version 查看版本号，出现版本号证明安装完成

## 2.快速搭建博客

选择你要存放你的博客的文件夹，在该文件夹进入你所使用的终端，使得终端上显示的路径是你当前所在文件夹的路径

进入 [Hugo 官网](https://gohugo.io/) ，点击 Quic Start 快速开始， 从 Step 2 开始将每个步骤的代码复制至你的终端中直至 Step 7

### 注意事项
1. Step 2 中的 quickstart 为你的博客的仓库的名字，最好设置为以你的 GitHub 的用户名开头的名字， 例如 zhangsan.github.io-creator
2. Step 3 中进入的文件夹为你在 Step 2 中设置的仓库名
3. Step 4 中的 my-first-post.md 为你的博客的名字，你也可以设置为 我的第一篇博客.md 或其他
4. 运行完 Step 4 的命令后你的博客已经建成，路径为 当前目录\content\posts\我的第一篇博客.md ，可以打开该文件进行编辑，如 Step 4 所说，你所能编辑的区域为 --- 以下的区域，编辑完你的博客后想要预览你的博客需要将 draft 改为 false
5. 运行了 Step 5 的命令后，可以点击命令行中的地址( 例如： http://localhost:1313/ )来预览你的博客，注意预览完不要按 Ctrl+C 退出，以便后面方便你预览修改了的博客
6. 打开一个新的终端来运行 Step 7 的命令，新终端上显示的路径应与你当前终端一致，进入 public 文件夹中

## 3.将你的博客上传到 GitHub 上

在 zhangsan.github.io-creator 文件夹中新建一个 .gitignore 文件，在 .gitignore 文件中输入 /public/ ，使得 public 能自成一个仓库

对 public 进行 git 操作，然后在你的 GitHub 上新建一个仓库，名字最好取为你的博客仓库的名字去掉 -creator ，例如 zhangsan.github.io ，接着将你的本地 git 仓库推送上去

在 GitHub 的仓库中点击 Settings ，找到 GitHub Pages ，如果在 Source 中有出现按钮则将其选择为 master ，完成后点击 Source 上方的地址，该地址即为你之前编辑的博客的地址，如果看到你的博客页面就说明你成功地用 Hugo 搭建了你的博客
