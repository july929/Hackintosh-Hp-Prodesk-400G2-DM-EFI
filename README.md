# Hackintosh Hp-Prodesk-400G2-DM OpenCore 0.6.5 EFI
![macOS Big Sur][1]


**电脑参数：**[Hp Prodesk 400G2  DM][2]

|配置|型号|
|----|----|
|系统|macOS Big Sur 11.1|
|CPU|Intel Core i5-6600t @ 2.7GHz 4核4线程|
|显卡|Intel HD Graphics 530 1536 MB|
|内存|金士顿 DDR4 2133MHz 16GB|
|硬盘|西数 SN550 256GB（NVMe SSD）|
|网卡|BCM943224PCIEBT2/AC 7265|
|声卡|Realtek ALC221|
|SMBIOS|Mac mini (2018)| 
|BIOS|N23 Ver.02.49 07/12/2020| 
|引导|OpenCore 0.6.5| 

**网卡将自带原装的`Intel AC 7265` 换成了博通的`BCM943224PCIEBT2`，这块网卡某宝大概卖20来块，2.4/5G 300M 蓝牙4.0 相比自带AC 7265 网速有一定的提升还支持隔空投送。**

## 实现功能
- CPU 睿频变频正常
- 核显 HD530 显存 1536MB
- 定制 USB2.0(内建鼠标/键盘)/USB3.0
- 声卡 内建 layout-id 为 11
- 有线网卡
- 无线正常(`BCM943224PCIEBT2`/`AC7265`)
- 蓝牙正常 (`BCM943224PCIEBT2`/`AC7265`)

## 存在问题
- 麦克风接口不工作；
- `macOS Big Sur 11.1`睡眠后无法唤醒会睡死，临时方案`节能`选项拉到`从不`即可；

## 更新日志

- 2021年01月15日
- 支持macOS Big Sur 11.1版本；
- 更新到 OpenCore 官方原版 0.6.5,使用OpenCanopy图形界面;
- 加入`BCM943224PCIEBT2`/`AC7265`网卡支持，默认BCM943224网卡config配置文件；
- 定制USB接口；键盘鼠标必须插到背后的USB2.0接口才能用；
- Kexts 更新到目前最新版 `2021-01-15`；

## BIOS设置
只需要注意这几项即可，其他按自己爱好设置即可。
- Secure Boot 关闭
- Fast Boot 关闭
- VTd 关闭
- 显存大小 >64M'

## 截图预览
![macOS Big Sur][3]
![OpenCore][4]

 [1]: https://i.loli.net/2021/01/15/Z9yUQOxhW1EClpM.png
 [2]: https://support.hp.com/ie-en/document/c04843458
 [3]: https://i.loli.net/2021/01/15/jIrfAZgkSL97GeO.png
 [4]: https://i.loli.net/2021/01/15/z1iVQSgwUGPZkKv.png
