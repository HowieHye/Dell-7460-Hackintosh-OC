# Dell-7460-Hackintosh-OC

自用EFI

## 说明

此 EFI 适用于戴尔燃 7000 系列第二代型号为 7460 的笔记本电脑。

## 电脑配置

| 规格     | 型号                               |
| -------- | ---------------------------------- |
| 电脑型号 | Dell Inspiron 7460                 |
| 操作系统 | macOS Big Sur Beta4(20A5343i)      |
| 处理器   | Intel Core i7-7500U @ 2.70GHz 双核 |
| 声卡     | ALC256                             |
| 网卡     | 已更换为 DW1560                    |

## OC

- 支持`macOS Big Sur Beta1~Beta4`,理论上支持`macOS High Sierra/macOS Mojave/macOS Catalina`
- CPU 原生支持，变频正常
- 显卡原生支持，`Lilu+WEG`
- 声卡正常
- 无线网卡更换为`DW1560`
- 显示器亮度调节正常

## Hidpi

仓库地址:[一键开启 HIDPI](https://github.com/xzhih/one-key-hidpi)

> 在终端运行
> `bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"`
>
> `Big Sur`用户运行
> `bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/dev/hidpi.sh)"`

## 系统截图

![](https://cdn.jsdelivr.net/gh/HowieHye/CDN@1.0.3/img/20200805221740.png)
![](https://cdn.jsdelivr.net/gh/HowieHye/CDN@1.0.3/img/20200805221739.png)
![](https://cdn.jsdelivr.net/gh/HowieHye/CDN@1.0.3/img/20200805221738.png)
![](https://cdn.jsdelivr.net/gh/HowieHye/CDN@1.0.3/img/20200805221737.png)
![](https://cdn.jsdelivr.net/gh/HowieHye/CDN@1.0.3/img/20200805221736.png)
![](https://cdn.jsdelivr.net/gh/HowieHye/CDN@1.0.3/img/20200805221735.png)

## 更新

- 2020-08-05
	- 更新`OC0.6.0`
- 2020-08-06
	- 更新`config.plist` , 修复安装/进入`Recovery`时显示俄语的错误
	- 已经测试`Big Sur Beta3`全新引导安装

## 鸣谢

- [@黑果小兵](https://github.com/daliansky/)
- [@冰水加劲](https://github.com/xzhih/)