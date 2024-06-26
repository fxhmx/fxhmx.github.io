# Node.js 安装及环境配置教程Windows

## 1. 下载 Node.js 安装包

首先，访问 [Node.js 官方](https://nodejs.org)网站 。在首页上，你会看到两个主要版本：LTS（长期支持版）和 Current（最新版）。对于大多数开发需求，推荐选择 LTS 版本，因为它更稳定。

**下载步骤**：

> 点击“LTS”版本旁边的“Windows Installer”链接下载 `.msi` 安装包。
>
> 选择适合您系统的版本（通常是 Windows x64）。
>
> 下载完成后，保存安装包到您容易找到的位置。

## 2. 安装 Node.js

**安装步骤**：

> 双击下载的 `.msi` 文件开始安装。
>
> 安装向导会打开，点击“Next”继续。
>
> 接受许可协议，再次点击“Next”。
>
> 选择安装路径。默认情况下，Node.js 会安装到 `C:\Program Files\nodejs\`。除非有特殊需求，建议使用默认路径。
>
> 点击“Install”开始安装。
>
> 安装完成后，点击“Finish”完成安装。

## 3. 验证安装

**验证步骤**：

> 打开命令提示符（CMD）。
>
> 输入 `node -v` 并回车，如果看到 Node.js 的版本号，说明 Node.js 安装成功。
>
> 接着输入 `npm -v` 并回车，如果看到 npm 的版本号，说明 npm 也安装成功。

## 4. 配置环境变量

为了方便在任何目录下使用 Node.js 和 npm 命令，需要将它们添加到系统环境变量。

**配置步骤**：

> 右键点击“此电脑”或“我的电脑”，选择“属性”。
>
> 点击“高级系统设置”。
>
> 在“系统属性”窗口中，点击“环境变量”按钮。
>
> 在“系统变量”区域中，找到并选择“Path”变量，然后点击“编辑”。
>
> 点击“新建”，添加 Node.js 的安装路径（例如 `C:\Program Files\nodejs\`）。
>
> 确认并关闭所有打开的窗口。

## 5. 配置 npm

npm 是 Node.js 的包管理器，用于安装和管理 Node.js 模块。

**配置步骤**：

在命令提示符中输入以下命令来设置 npm 的全局安装路径和缓存路径：

```
npm config set prefix "C:\Program Files\nodejs\node_global"
npm config set cache "C:\Program Files\nodejs\node_cache"
```

> 创建 `node_global` 和 `node_cache` 文件夹（如果它们不存在）。
>
> 再次编辑“系统变量”中的“Path”，添加 `C:\Program Files\nodejs\node_global`。

## 6. 使用国内镜像源

由于网络原因，使用 npm 安装模块时可能会遇到速度慢或失败的问题。可以使用淘宝 NPM 镜像加速安装过程。

**配置步骤**：

在命令提示符中输入以下命令：

```
npm config set registry https://registry.npmmirror.com
```

## 7. 完成

现在，您已经成功安装并配置了 Node.js 和 npm。您可以开始使用 Node.js 进行 Web 开发或运行其他 Node.js 应用程序了。
