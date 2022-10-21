# Dell-7460-Hackintosh-OC

EFI使用有问题？请参考这篇文档[黑苹果安装指北手册](https://howiehye.top/post/9ff9620/)

## 说明

~~由于我已经更换`Macbook Air`，所以本仓库不再更新维护，`OC`最终版本为`0.6.7`~~

Attention: Busy with study, not update frequently.

`Universal Control`没弄出来，不晓得啥情况。

此 EFI 适用于戴尔燃 7000 系列第二代型号为 7460 的笔记本电脑。

> ACPI Hotpatch来自[OC-little](https://github.com/daliansky/OC-little)

## 电脑配置

| 规格     | 型号                                        |
| -------- | ------------------------------------------- |
| 电脑型号 | `Dell Inspiron 7460`                        |
| 操作系统 | `macOS Ventura 13.0 RC 2 (22A380)` && `Windows 10` |
| 处理器   | `Intel Core i7-7500U @ 2.70GHz` 双核        |
| 声卡     | `ALC256`                                    |
| 网卡     | 已更换为 `DW1560`                           |

## OC

- OC版本：0.8.5
- 支持安装、升级和日常使用（不能保证都可以顺利安装, 只测试了安装macOS Ventura RC 1）
- 支持`macOS Monterey、macOS Ventura 13.0 RC`,理论上支持`macOS High Sierra/macOS Mojave/macOS Catalina/macOS Big Sur`
- CPU 原生支持，变频正常
- 显卡原生支持，`Lilu+WEG`
- 声卡正常
- 无线网卡更换为`DW1560`
- 显示器亮度调节正常

## CFG

**最新的 macOS Monterey 下没测试，自行测试**

CFG解锁 -> https://howiehye.top/post/7a13585/

出现任何硬件问题本人不负责任。

EFI 默认的`config.plist`是解锁CFG之后的，如果你未解锁，请将`config.plist`随便重命名，然后将`config_locked.plist`重命名为`config.plist`后使用。

## Hidpi

xzhih的脚本在macOS Monterey下未做测试，自行测试

推荐另外一个项目[BetterDummy](https://github.com/waydabber/BetterDummy)

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

- 每次升级或替换新的`EFI`后 , 最好重置一下`NVRAM`

## 鸣谢

- [黑果小兵](https://github.com/daliansky/)
- [冰水加劲](https://github.com/xzhih/)
- [Xjn's Blog](https://blog.xjn819.com/)
- [Steve Zheng](https://github.com/stevezhengshiqi)
- [Sukka](https://github.com/SukkaW)
