# Dell-7460-Hackintosh-OC

自用EFI

## 说明

此 EFI 适用于戴尔燃 7000 系列第二代型号为 7460 的笔记本电脑。

## 电脑配置

| 规格     | 型号                               |
| -------- | ---------------------------------- |
| 电脑型号 | `Dell Inspiron 7460`                 |
| 操作系统 | `macOS Big Sur Public Beta1(20A5343i)` && `Windows 10` && `Deepin V20`      |
| 处理器   | `Intel Core i7-7500U @ 2.70GHz` 双核 |
| 声卡     | `ALC256`                             |
| 网卡     | 已更换为 `DW1560`                    |

## OC

- 支持`macOS Big Sur Devloper Beta1~Beta4、macOS Big Sur Public Beta1`,理论上支持`macOS High Sierra/macOS Mojave/macOS Catalina`
- CPU 原生支持，变频正常
- 显卡原生支持，`Lilu+WEG`
- 声卡正常
- 无线网卡更换为`DW1560`
- 显示器亮度调节正常

## Hidpi

仓库地址:[一键开启 HIDPI](https://github.com/xzhih/one-key-hidpi)

> 在终端运行
>
> ```bash
> bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
> ```
>  
> `Big Sur`用户运行
>  
> ```bash
> bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/dev/hidpi.sh)"
> ```

## 系统截图

![更新截图](https://img.howiehye.top//img/20200807203611.png)

![关于本机](https://img.howiehye.top//img/20200807204722.png)

![控制中心](https://img.howiehye.top//img/20200807204844.png)

![Wi-Fi](https://img.howiehye.top//img/20200807204949.png)

![蓝牙](https://img.howiehye.top//img/20200807205020.png)

![Hacintool](https://img.howiehye.top//img/20200807205115.png)

## LOG

- 2020-08-05
  - 更新`OC0.6.0`
- 2020-08-06
  - 更新`config.plist` , 修复安装/进入`Recovery`时显示俄语的错误
  - 已经测试`Big Sur Beta3`全新引导安装
- 2020-08-07
  - `Big Sur Developer Beta4(20A5343i)`OTA升级`Big Sur Public Beta1(20A5343j)`

## 鸣谢

- [@黑果小兵](https://github.com/daliansky/)

- [@冰水加劲](https://github.com/xzhih/)
