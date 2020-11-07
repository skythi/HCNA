* 进入console用户界面
```conf
user-intercface console 0
```
* 配置用户界面  
在console用户界面视图下配置验证方式为Password验证，并配置密码为admin@123,且密码以明文方式保存在配置文件中
```conf
authentication-mode password 
set authentication password cipher admin@123
```
____
* 保存当前配置
将配置文件保存到文件名为backup.zip配置文件中，作为对vrpcfg.zip的备份
```conf
save backup.zip
```
* 设置下次启动的配置文件
```conf
startup saved-configuration back
```