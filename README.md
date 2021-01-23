# MSI-b450m-OC
### EFI概述

> 通过 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 按步骤配置
>

MacOS 版本：11.1 (20C69) Big Sur

Opencore 版本：0.6.5

更新日期：2021-01-23



### 配置清单

| 类型 | 型号              |
| ---- | ----------------- |
| 主板 | 微星 B450m 迫击炮 |
| CPU  | AMD R5 3600x      |
| 显卡 | 蓝宝石 VEGA 56    |



### 功能测试

##### 正常使用功能

* 前后端声音输出
* 所有USB端口
* 有线网络
* 蓝牙
* 接力
* 电源管理
* iMessage、FaceTime
* 独显硬件加速
* 睡眠/唤醒（修复XCH0端口问题需要修改IO属性到PTXH一致, 主板一致可直接使用）



### BIOS推荐设置

* 高级 -- windows操作系统的配置 -- `CSM` 改为 `UEFI`
* 高级 -- windows操作系统的配置 -- 安全引导 -- 禁止安全启动（默认禁止）
* 高级 -- USB设置 -- XHCI Hand-off -- 开启（默认开启）



### 注意事项

1. **登陆Apple ID前请先使用`Hackintool`等工具重新生成序列号等信息，避免与他人重复**
2. 如遇到黑屏情况，请尝试加启动参数`agdpmod=pikera`
3. 默认注入声卡`ID`为`1`，如不能正常工作请尝试更换启动参数中`alcid=1`的值
4. 默认使用`RealtekRTL8111.kext`，其他有线网卡自行更换


### 致谢

* [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html)
