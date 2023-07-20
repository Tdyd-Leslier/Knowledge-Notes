# GitHub 仓库文件上传

大多数新手第一次上传 GitHub 仓库文件都会遇到一些困难，这里记录了 GitHub 仓库文件上传的全过程，以及报错解决方法。

## 1. 前期准备

### 1.1 创建 GitHub 账号

请在 <https://github.com> 创建账号。

### 1.2 创建仓库

你可以创建新的仓库，也可以选择已有的仓库。如果选择已有的仓库，则无需创建。后续文件将会上传至所选择的仓库。

### 1.3 下载并安装 Git

Git 是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。 GitHub 是基于 Git 的代码库托管站，因此上传文件至 GitHub 就需要用到 Git ，可以在 <https://git-scm.com/downloads> 选择对应操作系统的安装包进行下载并安装。

### 1.4 创建文件夹

创建一个文件夹，将你要上传的文件放入其中。

## 2. 文件上传

好了，我们现在可以正式上传文件了。以下是通过 Git 命令来对文件进行操作，当然你也可以通过 Git UI 界面来对文件进行操作，但为了更好地理解 Git 的工作原理以及使用方法，还是推荐使用 Git 命令。

- 下面是以实操为例，首先，右键点击需要上传的文件，选择 ` Open Git Bash here ` ，这时候会进入 Git 命令窗口。

![1](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Knowledge-Notes/Git-Notes/2.1.jpg)

- 第一次上传文件需要克隆 GitHub 远程仓库到本地仓库中。

```git
git clone https://github.com/Tdyd-Leslier/Knowledge-Notes.git
```

![2](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Knowledge-Notes/Git-Notes/2.2.jpg)

- 为避免更换设备后，使用另一台设备上传文件时出现版本冲突的情况，你可以输入以下命令来确认当前远程仓库里的文件是最新版本。

```git
git pull origin main
```

![3](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Knowledge-Notes/Git-Notes/2.3.jpg)

- 提交本地文件。

```git
git add .
```

- 将提交的文件上传至暂存区。

```git
git commit -m "（这里填写你的备注，如 First commit ）"
```

注意：第一次使用会出现以下情况，你需要输入 GitHub 邮箱和用户名。

![4](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Knowledge-Notes/Git-Notes/2.4.jpg)

```git
git config --global user.email "（这里填写 GitHub 的邮箱）"
git config --global user.name "（这里填写 GitHub 的用户名）"
```

![5](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Knowledge-Notes/Git-Notes/2.5.jpg)

- 将暂存区的文件上传至远程仓库中。

```git
git push origin main
```

![6](https://tdydleslier-picgo.oss-cn-guangzhou.aliyuncs.com/Knowledge-Notes/Git-Notes/2.6.jpg)

- 后续上传文件只需反复执行以下命令即可。

```git
git add .
git commit -m "(这里填写你的备注，如 First commit)"、
git push origin main
```

好了，到这里你就可以成功地把文件上传到 GitHub 上了。

## 3. 报错解决

- 你可能会遇到 `Failed to connect to github.com port 443: Operation timed out` 。不用担心，如果你使用的是 Clash 或者 V2rayN 端口，可以输入以下命令。

```git
Clash端口
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890

V2rayN端口
git config --global http.proxy http://127.0.0.1:10809
git config --global https.proxy http://127.0.0.1:10809
```
