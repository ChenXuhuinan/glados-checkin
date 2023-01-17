# glados-checkin
  每天自动签到（天数+1），自动推送结果  

# clash 使用教程：  
  http://www.xmstudent.ml/post-24.html
  
 

# glados 注册
  [注册链接：https://glados.rocks/](https://glados.rocks/)   
  注：先复制下面激活码，注册后送3天，包月（10g），如果有教育邮箱可以使用教育plan（360天）（50g）  
      （若是普通邮箱注册，可更改为.edu邮箱，点下面的 for education 进行申请）  
  填写激活码：  **LMKGQ-4DJ97-XDQFX-VYUY4** 获得3天  
  
  我相信你们人手一堆教育邮箱，这个网站风控还行 
![](http://tu.yaohuo.me/imgs/2020/06/ed0e944eec323a16.png)

# Github Actions说明
## 一、Fork此仓库
![](http://tu.yaohuo.me/imgs/2020/06/f059fe73afb4ef5f.png)
## 二、设置账号密码

添加名为——值分别为：  
**SERVE**  ——**on/off** 你想你的serve酱开不开启通知  
**SCKEY**  ——**sckey**  开的话填你的serve酱的sckey，不开就不填   
**COOKIE** —— **cookie** 弄上你账号的cookie  
暂不支持多账号，懒得弄
![](http://tu.yaohuo.me/imgs/2020/06/748bf9c0ca6143cd.png)

**获取COOKIE**
登录glados，按键盘上的F12打开开发者工具

进入我的账户，刷新页面

如图所示找到cookie，把 cookie： 后面的几行都复制下来，填入上一步对应的value中

**获取SCKEY**
（2022.3.23更新：server酱的网站更新了，之前叫SCKEY，现在叫SENDKEY，但是不影响我们后面的操作）

这是在server酱中获取的，用于绑定微信，给你推送签到后的结果

server酱地址：https://sct.ftqq.com/login

## 三、启用Action
1 点击**Action**，再点击**I understand my workflows, go ahead and enable them**  
2 修改任意文件后提交一次  
![](http://tu.yaohuo.me/imgs/2020/06/34ca160c972b9927.png)

## 四、查看运行结果
Actions > Cloud189Checkin > build  
能看到如下图所示，表示成功，或者看你微信通知  
![](http://tu.yaohuo.me/imgs/2020/06/289432b53bded61c.png)  
  
# 腾讯云函数
复制py代码，将三个参数自行修改  


自此就成功了，每天凌晨12点多都会自动签到的，**不过cookie过段时间会失效，到时登录github手动更改一下cookie值就行**。
若有需求，可以在[.github/workflows/python-publish.yml]中自行修改  
