# Dell-7460-Hackintosh-OC

EFI使用有问题？请参考这篇文档[黑苹果安装指北手册](https://howiehye.top/post/9ff9620/)

## 说明

此 EFI 适用于戴尔燃 7000 系列第二代型号为 7460 的笔记本电脑。

> ACPI Hotpatch来自[OC-little](https://github.com/daliansky/OC-little)

从`Clover`转向`OC`的用户，请清理`Clover`残余

此部分内容摘自Sukka的[从 Clover 到 OpenCore —— Clover 迁移 OpenCore 指南 | Sukka's Blog](https://blog.skk.moe/post/from-clover-to-opencore)

重启到 OpenCore 引导之前，务必清理掉 Clover 的残留文件：

```shell
# 删除 Clover 位于系统偏好设置中的面板
sudo rm -rf "/Library/PreferencePanes/Clover.prefPane"
# 删除 Clover 的自动脚本
rm -rf "/etc/rc.clover.lib"
rm -rf "/etc/rc.boot.d/10.save_and_rotate_boot_log.local"
rm -rf "/etc/rc.boot.d/20.mount_ESP.local"
rm -rf "/etc/rc.boot.d/70.disable_sleep_proxy_client.local.disabled"
rm -rf "/etc/rc.boot.d/80.save_nvram_plist.local"
rm -rf "/etc/rc.shutdown.local"
rm -rf "/etc/rc.boot.d"
rm -rf "/etc/rc.shutdown.d"
# 删除 Clover 的守护进程
launchctl unload '/Library/LaunchDaemons/com.slice.CloverDaemonNew.plist'
rm -rf '/Library/LaunchDaemons/com.slice.CloverDaemonNew.plist'
rm -rf '/Library/Application Support/Clover/CloverDaemonNew'
rm -rf '/Library/Application Support/Clover/CloverLogOut'
rm -rf '/Library/Application Support/Clover/CloverWrapper.sh'
```

除此以外，在使用 OpenCore 引导 macOS 之前需要重置 NVRAM。如果你之前使用的是模拟 NVRAM，那么还需要删除 EFI 分区中的 nvram.plist 文件。

- 如果在 OpenCore 中启用了 AllowNvramReset 这个 Quirk，那么可以在 OpenCore 引导菜单中，按下空格键显示隐藏条目，最后一个条目就是 OpenCore 内置的重置 NVRAM 功能。
- 也可以在 Clover 中重置 NVRAM：删除模拟 NVRAM 驱动和 nvram.plist 以后，在 Clover 引导菜单中按下 F11 来清除 NVRAM。

## 电脑配置

| 规格     | 型号                                        |
| -------- | ------------------------------------------- |
| 电脑型号 | `Dell Inspiron 7460`                        |
| 操作系统 | `macOS Big Sur 11.2.2(20D80)` && `Windows 10` |
| 处理器   | `Intel Core i7-7500U @ 2.70GHz` 双核        |
| 声卡     | `ALC256`                                    |
| 网卡     | 已更换为 `DW1560`                           |

## OC

- OC版本：0.6.7
- 支持安装、升级和日常使用（不能保证都可以顺利安装，安装或升级时请自行在`boot-args`里添加`-v`）
- 支持`macOS Catalina、macOS Big Sur Beta`,理论上支持`macOS High Sierra/macOS Mojave`
- CPU 原生支持，变频正常
- 显卡原生支持，`Lilu+WEG`
- 声卡正常
- 无线网卡更换为`DW1560`
- 显示器亮度调节正常

## CFG

CFG解锁 -> https://howiehye.top/post/7a13585/

出现任何硬件问题本人不负责任。

EFI 默认的`config.plist`是解锁CFG之后的，如果你未解锁，请将`config.plist`随便重命名，然后将`config_locked.plist`重命名为`config.plist`后使用。

## Hidpi

仓库地址:[一键开启 HIDPI](https://github.com/xzhih/one-key-hidpi)

> 在终端运行
>
> ```bash
> bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
> ```
>
> 网络不好的可以用这条
>
> ```bash
> bash -c "$(curl -fsSL https://gitee.com/howiehye/one-key-hidpi/raw/master/hidpi.sh)"
> ```

## 截图

![02034029](https://cdn.jsdelivr.net/gh/HowieHye/CDN@master/img/02034029.4wq9mpvmx5s0.png)

![2020-11-08-19-49](https://img.howiehye.top//img/2020-11-08-19-49.png)

![2020-11-08-19-53](https://img.howiehye.top//img/2020-11-08-19-53.png)

## 其他说明

- 安装`macOS Big Sur`的过程很漫长 , 请耐心等待 , 不一定是有错误
- 每次升级或替换新的`EFI`后 , 最好重置一下`NVRAM`

## 鸣谢

- [黑果小兵](https://github.com/daliansky/)
- [冰水加劲](https://github.com/xzhih/)
- [Xjn's Blog](https://blog.xjn819.com/)
- [Steve Zheng](https://github.com/stevezhengshiqi)
- [Sukka](https://github.com/SukkaW)
