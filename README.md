# [提问箱](http://172.81.235.232:8080/mesBoard_Web_exploded/login.html)

## 一、项目概述：
    提问者匿名，回答者公开。

## 二、项目地址：  
    提问箱: :http://172.81.235.232:8080/mesBoard_Web_exploded/login.html
   
## 三、注册登录与忘记密码：
     1.注册。（需要输入，用户名、密码、确认密码、邮箱、验证码。）
        1.1 用户名：目前未对用户名有限制（如中英文，特殊符号）。
        1.2 密码：密码必须为大于8位的数字和字母和其他字符组合。（不符合要求页面会提示，密码hash后传送给后端）
        1.3 确认密码：与密码一致，（页面会给出提示）。
        1.4 邮箱：前端和后端都有对邮箱格式正确性进行校验。（一般格式：..XXX@XX.com）
        1.5 验证码：字母与数字混合。
     2. 账号激活。（注册成功向邮箱发送激活邮件）
      	2.1  激活邮件中的激活链接含有唯一标识码，标识该用户的激活。
     3. 登录  
      	3.1.可使用用户名或邮箱登录。
      	3.2. 验证码：字母与数字混合。
     4.忘记密码（重置密码）
      	4.1 输入邮箱，若邮箱有效将发送重置密码链接，重置密码链接含有唯一标识码，标识该用户的本次密码重置。
      	4.2 重置密码：为提升用户体验，需输入密码和确认密码，其满足条件同注册。
      	4.3 每次重置密码将唯一标识符存入数据库，用作检验token的密钥，从将非法用户踢下线。
      	
## 四、用户资料管理：
		1. 用户名：用户名唯一，故更改用户名同名，不能成功更改。并给出提示。
		2. 邮箱：更改邮箱需要输入密码验证并重新激活。
			2.1. 若注册时输错邮箱可凭密码更改邮箱重新激活账户。
			2.2. 邮箱唯一，故更改邮箱已存在，不能更改，并给出提示。
		3.密码：
		 	3.1.通过提供原密码来修改密码。
		 	3.2.为提升用户体验，需输入密码和确认密码，其满足条件同注册。
		 	3.3.更改密码同忘记密码（4.3），可将用户踢下线
		 4.头像（可更换头像）
		   4.1.超大文件，前端后端都有判断，不允许超过1M
		   4.2.前端后端都有判断只允许图片的后缀名，(jpg,png等）
		   4.3.文件名有+UUID，故实际存储不会相同。
		  5.提问箱（可以在个人资料中设置开启关闭）
		  
## 五、提问箱管理：
	5.1. 提问箱激活成功后，默认提问箱打开，接受其他用户的提问，也可以发起提问。
![提问](https://img-blog.csdnimg.cn/2020050122461055.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzODA1MDUz,size_16,color_FFFFFF,t_70#pic_center)
