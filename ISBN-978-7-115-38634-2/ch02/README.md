### VRP
VRP(Versatile Routing Platform)，华为公司数通产品得通过网络操作系统  
<table>
        <tr>
            <th>用户级别</th>
            <th>命令级别</th>
            <th>说明</th>
        </tr>
        <tr>
            <th>0</th>
            <th>0</th>
            <th>网络诊断命令,从本设备访问其他设备得命令</th>
        </tr>
        <tr>
            <th>1</th>
            <th>0、1</th>
            <th>系统维护命令，包括部分display</th>
        </tr>
        <tr>
            <th>2</th>
            <th>0、1、2</th>
            <th>业务配置命令，包括路由，各个网络层次得命令</th>
        </tr>
        <tr>
            <th>3~15</th>
            <th>0、1、2、3</th>
            <th>设计系统基本运行得命令，如文件系统，FTP下载，配置文件切换，用户管理命令，命令级别设别，包括debugging</th>
        </tr>
    </table>

___
### 配置设备系统时钟
设置时区和设备当前的日期和时间  
clock timezone time-zone-name {add|minus} offset
```conf
clock timezone BJ add 08:00
clock datetime 22:25 2020-10-24
```
___
#### 配置设备IP地址
假设设备的管理接口为Ethernet 1/0/0,分配地址为10.1.1.100，子网掩码为255.255.255.0
```conf
<HUAWEI> system-view 
[HUAWEI] interface MEth 0/0/1
```
执行命令ip address ip-address { mask | mask-length }，配置MEth接口的IP地址。此处假设设备管理网口的IP地址为10.1.1.100/24
```conf
[HUAWEI-MEth0/0/1] ip address 10.1.1.1 24
```