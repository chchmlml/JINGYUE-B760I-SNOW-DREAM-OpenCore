## 精粤 B760I SNOW DREAM 黑苹果 OpenCore EFI

![image](ScreenShot/JINGYUEB760I.png)

### OpenCore

[OpenCore 1.0.2](https://github.com/acidanthera/OpenCorePkg)

### support macOS

| macOS Version | Version Number |
| ------------- | -------------- |
| macOS Monterey | 12.x           |
| macOS Ventura  | 13.x           |
| macOS Sonoma   | 14.x           |
| macOS Sequoia  | 15.x           |

### 硬件

| 组件         | 型号/规格                                   |
| ------------ | ----------------------------------------- |
| 芯片组       | B760                                       |
| BIOS 版本    | JYI7600F 2025-01-07                        |
| 处理器       | 英特尔 13代 i5-13400F                      |
| 内存         | 酷兽 32GB DDR4 3600MHz                     |
| 硬盘         | 梵想 Fanxiang S790 1TB Windows             |
| 核显         | --                                         |
| 独显         | 技嘉 Radeon RX 6600 8GB GDDR6              |
| 声卡         | 瑞昱 ALC897                                |
| 有线网卡     | 瑞昱 RTL8125 Gaming 2.5GbE                |
| 有线网卡     | 瑞昱 RTL8168H/8111H                        |
| 无线网卡     | Intel AX211                                |
| 处理器散热   | 利民 CS120                                 |
| 机箱         | 乔思伯 D32 STD                             |
| 电源         | 利民 额定650W TR-TG650 金牌全模组          |


### BIOS设置

```
高级
     |-- CPU电源管理控制
        |-- CPU锁配置
	         |-- CFG锁定：关闭
	   |-- PCI总线驱动版本     
	       |-- Re-Size BAR Support：Disabled
     |-- CSM配置
	      |-- CSM支持：关闭
		
启动
  |-- 安全启动
    |-- 安全启动：关闭
```

### 注意事项

 - 安装成功后必须使用 [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) 生成你自己的 SMBIOS
 - 如需使用没有小核心的CPU，必须取消勾选配置文件中Kernel--ProvideCurrentCpuinfo选项
 - 无线网卡方案有两种
   - 英特尔无线网卡驱动[itlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases)适用于 MacOS 所有版本,连结WiFi请下载并使用[HeliPort.dmg](https://github.com/OpenIntelWireless/HeliPort/releases/download/v2.0.0-alpha/HeliPort.dmg).
   - 下载并添加[AirportItlwm.kext驱动](https://github.com/OpenIntelWireless/itlwm/releases)，此驱动必须对应 MacOS 系统版本，添加驱动至EFI-OC-Kexts文件夹，[参考](https://hackintosh.club/d/10000015)
 - 英特尔无线网卡无法使用隔空投送等功能

### 参考内容

[1.黑苹果安装过程演示](https://hackintosh.club/d/10000060)

[2.英特尔无线网卡WiFi驱动](https://hackintosh.club/d/10000015)

[3.英特尔无线网卡蓝牙驱动](https://hackintosh.club/d/10000017)

[4.我的B站黑苹果教程](https://space.bilibili.com/244390800/video)

[6.黑果之家](https://hackintosh.club)


### 常用工具
- [OpenCore-Legacy-Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher)
- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) AKA `OCAT`.
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA `OCC`.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.
