# v23.8-passwall

因为 CatWrt 源提供的 pw 包有问题，所以没有内置，就算你们拉源去安装也是不能启动的这里看日志就看得出来，此问题影响 amd64 & mt798x 版本的 CatWrt


## x86

在 SSH CatWrt 终端中输入一下代码

```bash
wget -P /tmp https://ghproxy.com/https://github.com/xiaorouji/openwrt-passwall/releases/download/4.70-7/luci-i18n-passwall-zh-cn_git-23.256.63940-4bb0d98_all.ipk
wget -P /tmp https://ghproxy.com/https://github.com/xiaorouji/openwrt-passwall/releases/download/4.70-7/luci-app-passwall_4.70-7_all.ipk
cd /tmp
opkg install .tmp/luci-app-passwall_4.70-7_all.ipk
opkg install ./luci-app-passwall-zh-cn_4.70-7_all.ipk
```
## mt798x

按照博客

https://www.miaoer.xyz/posts/network/catwrt-install-application
https://www.miaoer.xyz/posts/network/catwrt-applist

拉取 CatWrt 源后安装 luci-app-passwall，随后卸载插件（请结合博客选择在终端使用命令安装还是在 LuCI 中安装）

注意这里的依赖组件不会卸载如果卸载了你需要记住后面再安装，执行上诉 x86 的命令即可安装。

开源软件来源: https://github.com/xiaorouji/openwrt-passwall 
与博主无关，仅供学习参考
