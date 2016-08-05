# Git 配置

Git 使用 `git config` 进行设置， 设置存储在三个不同的位置：

1. `/etc/gitconfig` 文件: 包含系统上每一个用户及他们仓库的通用配置。 可以传递 `--system` 选项让 Git 读写此文件。
2. `~/.gitconfig` 或 `~/.config/git/config` 文件：只针对当前用户。 可以传递 `--global` 选项让 Git 读写此文件。
3. 当前使用仓库的 Git 目录中的 config 文件（就是 `.git/config`）

每一个级别覆盖上一级别的配置，所以 .git/config 的配置变量会覆盖 /etc/gitconfig 中的配置变量。


## 用户信息

当安装完 Git 应该做的第一件事就是设置你的用户名称与邮件地址。 这样做很重要，因为每一个 Git 的提交都会使用这些信息，并且它会写入到你的每一次提交中，不可更改：
```git
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
当你想针对特定项目使用不同的用户名称与邮件地址时，可以在那个项目目录下运行没有 `--global` 选项的命令来配置。

## 文本编辑器

配置默认文本编辑器了，例如
```git
git config --global core.editor vim
```

## 检查配置信息

使用 `git config --list` 命令来列出所有 Git 当时能找到的配置。

## 获取帮助

有三种方法可以找到 Git 命令的使用手册：

1. `git help <verb>`
2. `git <verb> --help`
3. `man git-<verb>`


