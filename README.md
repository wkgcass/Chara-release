# Chara-release

## 最新版下载链接

| 名称                        | 分支                      | 类型                    | 版本                | 链接 |
|-----------------------------|---------------------------|-------------------------|---------------------|------|
| Chara                       | chara                     | 启动器                  | 1.0.0               | [macos](https://github.com/wkgcass/Chara-release/raw/release-chara-latest/chara.pkg) [windows](https://github.com/wkgcass/Chara-release/raw/release-chara-latest/chara.msi)
| 心璃 (kokori)               | kokori                    | 模型（人物）            | 1.0.0               | [kokori-high-dpi.model](https://github.com/wkgcass/Chara-release/raw/release-kokori-latest/kokori-high-dpi.model) [kokori-mini.model](https://github.com/wkgcass/Chara-release/raw/release-kokori-latest/kokori-mini.model) |
| console-plugin              | console                   | 插件                    | 1.0.0               | [console.plugin](https://github.com/wkgcass/Chara-release/raw/release-console-latest/console.plugin) |
| debug-plugin                | debug                     | 插件                    | 1.0.0               | [debug.plugin](https://github.com/wkgcass/Chara-release/raw/release-debug-latest/debug.plugin) |
| dev-plugin                  | dev                       | 插件                    | 1.0.0               | [dev.plugin](https://github.com/wkgcass/Chara-release/raw/release-dev-latest/dev.plugin) |
| noto-font-plugin            | noto-font                 | 插件                    | 1.0.0               | [noto-font.plugin](https://github.com/wkgcass/Chara-release/raw/release-noto-font-latest/noto-font.plugin) |
| r18-plugin                  | r18                       | 插件                    | 1.0.0               | [r18.plugin](https://github.com/wkgcass/Chara-release/raw/release-r18-latest/r18.plugin) |
| tianxing-chatbot-plugin     | tianxing-chatbot          | 插件                    | 1.0.0               | [tianxing-chatbot.plugin](https://github.com/wkgcass/Chara-release/raw/release-tianxing-chatbot-latest/tianxing-chatbot.plugin) |
| wqy-font-plugin             | wqy-font                  | 插件                    | 1.0.0               | [wqy-font](https://github.com/wkgcass/Chara-release/raw/release-wqy-font-latest/wqy-font.plugin) |
| vproxy                      | vproxy                    | 基础依赖（线程、网络）  | 1.0.0-BETA-11-DEV-1 | [vproxy.jar](https://github.com/wkgcass/Chara-release/raw/release-vproxy-latest/vproxy.jar) |

模型请在启动器中选择，首次启动时会直接弹出文件选择对话框，之后可以选择曾经加载过的模型  
插件请放置到`~/.chara/plugin`目录中，windows下对应`%userprofile%\.chara\plugin`目录，目录可能需要手动创建

## Chara

功能和演示请见[这里](http://blog.cassite.net/Chara)

## 分支

每个工程的每一个版本对应一个分支，你可以直接定位到指定的分支拉取打包好的二进制文件。例如：

```shell
git clone https://github.com/wkgcass/Chara-release --depth=1 --single-branch --branch=release-${project}-${version}
```

你也可以在github页面中浏览或搜索所有的分支，并直接下载。

此外，版本号`latest`代表该工程的最新版本，一般可以直接下载`release-${project}-latest`分支的二进制文件。

> 注意，当patch版本发布时，同minor version的release可能会被删除。不过不同的major或minor version的release都会保留。

## 临时分支

临时分支中的二进制文件可能随时被替换或移除。一般是用于存放快速修复了一些小bug的临时版本。临时分支命名：`temporary-${project}-${version}`。

## 分支内容

每个二进制文件都会有如下附属文件：

* {binary-file} 二进制文件本身
* {binary-file}.md5 二进制文件的md5值，hex小写字母
* {binary-file}.sha1 二进制文件的sha1值，hex小写字母
* {binary-file}.sha256 二进制文件的sha256值，hex小写字母
* version 版本号，和分支中的version一致，主要用于在latest分支上区分当前版本
