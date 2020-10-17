
~~~
 以后OC版本无重大更新或者不匹配MAC版本，将暂缓更新。  
 目前的EFI不能说无BUG，但是足够日常使用。坐等macOS11正式版。  
 有问题请在issues提问。  
~~~
~~~~~~
2020年10月17日
更新 `config.plist`适应bate10.  
更新OC版本到2020-10-17.   
更新`VirtualSMC`到最新.  
~~~~~~
| 硬件| 型号|   
| :----: | :---- |
| CPU | I5 6300HQ |    
|内存 | 8G*2 DDR4 |     
|显卡| Intel HD Graphics 530 + NVIDIA GeForce GTX 960M |     
|网卡| Realtek RTL8111H + BCM94352z |     
|声卡| Realtek ALC295  |   
## 系统支持
系统：macOS 11 B9  
EFI:OC0.6.2   
编译日期2020-10-07  
### 正常功能：  
1. 核心显卡
2. FN按键
3. 电源管理
4. 睡眠
5. 声音
6. 蓝牙
7. 触摸板
8. 摄像头
9. 无线网卡
10. 隔空投送  

# 注意:同系列使用我的EFI请注意APCI下的补丁 文件里面的APCI 命名是否和你们的DSDT里面一样.
具体SSDT是否通用请移步 小兵的仓库查看 [点击进入](https://github.com/daliansky/OC-little)  
## 例如:`SSDT-ALS0.aml` 仿冒环境光传感器补丁  

原始 `ACPI` 存在环境光传感器设备接口和不存在环境光传感器设备接口。首先在原始 `ACPI` 里面查找 `ACPI0008`，如果可以查到相关设备，一般是 `ALSD`，则说明存在环境光传感器设备接口，否则即为不存在环境光传感器设备接口。  

我的原始`ACPI`并没有存在`ACPI0008` 所以使用的是`SSDT-ALS0.aml`    

具体请进入 [这里查看](https://github.com/daliansky/OC-little/tree/master/02-%E4%BB%BF%E5%86%92%E8%AE%BE%E5%A4%87/02-4-%E4%BB%BF%E5%86%92%E7%8E%AF%E5%A2%83%E5%85%89%E4%BC%A0%E6%84%9F%E5%99%A8)  

# 问题
1. 双系统 会概率自动进WIN10 重启一次就可以进入mac 11.目前已优化配置并更新OC到6.2正式版，目前尚未出现自动进入WIN10的情况。  
      (已确认修复)  
