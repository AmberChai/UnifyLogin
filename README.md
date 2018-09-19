## 域名 ##

- 沙盒环境: https://sandbox-ul.uu.cc
- 正式环境: https://ul.uu.cc


## 1. 查询用户信息-[/player/search]

**简要描述：**
- 客服系统调用
- 支持pid,openid,手机号，用户名
- 需要配置IP白名单

**请求URL：** 


- http://xx.com/player/search
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| p  | string  |  N | 查询数据  |
| u  |  int |  N | 使用uid查询时使用 |



 **返回示例**

```
{
    "code": 0,
    "desc": "success",
    "result": {
        "player": {
            "1073491953_11074_Hphone_0": {
                "id": 349,
                "player_id": 1073491953,
                "game_id": 11074,
                "login_type": "Hphone",
                "login_name": "1073491953",
                "user_id": 1073491953,
                "channel_id": "AZ0S0N00002",
                "is_validity": 0,
                "to_login_ext": null,
                "last_device_id": "4849375rn3034_2922613qr042r6o9q1p",
                "last_login_time": 1529545092,
                "device_brand": "KNT-AL20",
                "IP": "192.168.119.66",
                "location": "20180620205306+0800",
                "create_time": 1529500575
            },
            "1073491953_10058_Huser_0": {
                "id": 350,
                "player_id": 1073491953,
                "game_id": 10058,
                "login_type": "Huser",
                "login_name": "1073491953",
                "user_id": 1073491953,
                "channel_id": "TEST0000000",
                "is_validity": 0,
                "to_login_ext": null,
                "last_device_id": "83q1q11n1_3229119054873088411r855",
                "last_login_time": 1529499208,
                "device_brand": "HONOR H30-L01",
                "IP": "192.168.119.66",
                "location": "20170927143129+0800",
                "create_time": 1529499208
            },
            "1073491953_11074_Huser_0": {
                "id": 351,
                "player_id": 1073491953,
                "game_id": 11074,
                "login_type": "Huser",
                "login_name": "1073491953",
                "user_id": 1073491953,
                "channel_id": "AZ0S0N00002",
                "is_validity": 0,
                "to_login_ext": null,
                "last_device_id": "4849375rn3034_2922613qr042r6o9q1p",
                "last_login_time": 1529545092,
                "device_brand": "KNT-AL20",
                "IP": "192.168.119.66",
                "location": "20180620205306+0800",
                "create_time": 1529500575
            }
        },
        "account": {
            "uid": 1073491953,
            "account_id": 1073491953,
            "nickname": "martinsun",
            "real_name": "伊彤",
            "card": "411102198511179236",
            "is_auth": 1,
            "email": "",
            "gender": "m",
            "avatar_url": "http://q.qlogo.cn/qqapp/101416814/7DFD75A71BC9C6F35C15A586F4DA4E90/100",
            "message": "这家伙很懒，什么都没有留下",
            "created": 1474617661,
            "update_time": 1529409726,
            "has_password": true,
            "phone": "13128783537",
            "birthday": "1985-11-17",
            "is_visitor": false,
            "city": "武汉",
            "address": "",
            "country": "",
            "province": "湖北"
        }
    }
}
```
- 返回数据说明

|  名称 | 类型  | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| code| int | 接口的响应值0为成功，其他失败，参考[错误码对应表](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/565.html "响应码对应表")| 
| desc | string  | 对应的说明（当code为4000时，可以为展示给玩家的提示） |
| result | object  | 响应的数据，一般请求成功则不为空，其他为空 |
| account | object  | 帐号信息 |
| uid | int | 帐号id |
| nickname | string | 昵称 |
| real_name | string | 真实姓名 |
| card | string | 身份证号 |
| is_auth | int | 是否认证 |
| email | string | 邮箱 |
| gender | string | 性别 |
| avatar_url | string | 头像地址 |
| created | int | 创建时间 |
| update_time | int | 更新时间 |
| has_password | int | 是否有密码 |
| phone | string | 手机号 |
| birthday | string | 出生日期 |
| city | string | 城市 |
| address | string | 地址 |
| country | string | 国家 |
| province | string | 省份 |
| player | object | 玩家id |
| player_id | int | 玩家id |
| game_id | int | 游戏id |
| login_type | string | 登录类型 |
| login_name | string | 登录名 |
| user_id | int | 帐号id |
| channel_id | string | 渠道号 |
| is_validity | int | 是否是游客 |
| to_login_ext | string | 扩展信息 |
| last_device_id | string | 最后登录设备 |
| last_login_time | int | 最后登录时间 |
| device_brand | string |手机类型 |
| IP | string | 客户端IP  |
| location | string | 本地时间 |
| create_time |  int |创建时间 |


## 2. 登录 [/sns/login]
**简要描述：**
- 社区. 微信商城，IPG等服务端调用接口API
- 需要配置IP白名单

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/login
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| login_name  | string  |  Y | 登录名 （可以是手机号或者用户名） |
| appkey  | string  |  Y | 应用key(没有应用请在dgc申请) |
| password  | string  |  N | 密码 |
| code | int | N | 验证码（详情参考备注说明） |
| grant_type | string | N | 平台选择返回数据类型是否需要授权码类型数据，固定值authorization_code |
| password  | string  |  N | 注册时是否设置密码有则传 |
| sign | string | N | 签名规则参考（[签名规则](http://dc.idreamsky.com/tongyizhanghaoxiangguanapijiek/show/140.html#h2--sign- "签名规则")） |

 **响应结果**
 ```
 {
    "code": 0,
    "desc": "success",
    "result": {
        "uid": 1073491953,
        "account_id": 1073491953,
        "nickname": "martinsun",
        "real_name": "伊彤",
        "card": "411102198511179236",
        "is_auth": 1,
        "email": "",
        "gender": "m",
        "avatar_url": "http://q.qlogo.cn/qqapp/101416814/7DFD75A71BC9C6F35C15A586F4DA4E90/100",
        "message": "这家伙很懒，什么都没有留下",
        "created": 1474617661,
        "update_time": 1529409726,
        "has_password": true,
        "phone": "13128783537",
        "birthday": "1985-11-17",
        "is_visitor": false,
        "city": "武汉",
        "address": "",
        "country": "",
        "province": "湖北"
    }
}
 ```
- grant_type模式响应结果
```
{
    "code": 0,
    "desc": "success",
    "result": {
        "token_key": "798dafbe9eac870fdbecf85882499e5d05b51acfc",
        "token_secret": "ba42d4386921b956e9c7cef15ee84549"
    }
}
```

## 3. 注册 [/sns/register]
**简要描述：**
- 社区. 微信商城，IPG等服务端调用接口API
- 需要配置IP白名单

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/register
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| mobile  | string  |  Y | 注册的手机号） |
| appkey  | string  |  Y | 应用key(没有应用请在dgc申请) |
| code | int | Y | 验证码（详情参考备注说明） |
| grant_type | string | N | 平台选择返回数据类型是否需要授权码类型数据，固定值authorization_code |
| password  | string  |  N | 注册时是否设置密码有则传 |
| sign | string |N | 签名规则参考（[签名规则](http://dc.idreamsky.com/tongyizhanghaoxiangguanapijiek/show/140.html#h2--sign- "签名规则")） |

- 备注
> `情景一`：注册验证码下发，是SDK服务器自己下发，验证码为纯数字型，则不需要做签名校验
`情景二`：注册验证码下发是非SDK服务器自己下发，则验证码为调用平台自定义值，且值为非数字的6位大写字母，接口需要签名操作
`grant_type`: 需要获取授权码，用于请求其它服务时需带参数

 **响应结果**
 ```
 {
    "code": 0,
    "desc": "success",
    "result": {
        "uid": 1073491953,
        "account_id": 1073491953,
        "nickname": "martinsun",
        "real_name": "伊彤",
        "card": "411102198511179236",
        "is_auth": 1,
        "email": "",
        "gender": "m",
        "avatar_url": "http://q.qlogo.cn/qqapp/101416814/7DFD75A71BC9C6F35C15A586F4DA4E90/100",
        "message": "这家伙很懒，什么都没有留下",
        "created": 1474617661,
        "update_time": 1529409726,
        "has_password": true,
        "phone": "13128783537",
        "birthday": "1985-11-17",
        "is_visitor": false,
        "city": "武汉",
        "address": "",
        "country": "",
        "province": "湖北"
    }
}
 ```
 
- grant_type模式响应结果
```
{
    "code": 0,
    "desc": "success",
    "result": {
        "token_key": "798dafbe9eac870fdbecf85882499e5d05b51acfc",
        "token_secret": "ba42d4386921b956e9c7cef15ee84549"
    }
}
```

## 4. 获取用户信息 [/sns/getUserinfo]
**简要描述：**
- 社区. 微信商城，IPG等服务端调用接口API
- 需要配置IP白名单
- 使用用户id（uid）和游戏id(game_id),查询查询玩家id(player_id)

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/getUserinfo
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| uid  | string  |  N | 用户id |
| game_id  | string  |  N | 游戏id |
| token | string | N | 登录成功返回的票据 |
| appkey | string | N | 应用appkey |

 **响应结果**
 - 使用uid,game_id 查询 用户信息 
 ```
 {
    "code": 0,
    "desc": "success",
    "result": {
        "player": {
            "id": 466,
            "game_id": 11074,
            "player_id": 1073491953,
            "login_type": "Hphone",
            "login_name": "1073491953",
            "user_id": 1073491953,
            "is_validity": 0,
            "to_login_ext": null,
            "last_device_id": "4849375rn3034_2922613qr042r6o9q1p",
            "last_login_time": 1529545092,
            "channel_id": "AZ0S0N00002",
            "device_brand": "KNT-AL20",
            "IP": "192.168.119.66",
            "imei": "",
            "location": "20180620205306+0800",
            "create_time": 1529500575
        },
        "account": {
            "uid": 1073491953,
            "account_id": 1073491953,
            "nickname": "martinsun",
            "real_name": "伊彤",
            "card": "411102198511179236",
            "is_auth": 1,
            "email": "",
            "gender": "m",
            "avatar_url": "http://q.qlogo.cn/qqapp/101416814/7DFD75A71BC9C6F35C15A586F4DA4E90/100",
            "message": "这家伙很懒，什么都没有留下",
            "created": 1474617661,
            "update_time": 1529409726,
            "has_password": true,
            "phone": "13128783537",
            "birthday": "1985-11-17",
            "is_visitor": false,
            "city": "武汉",
            "address": "",
            "country": "",
            "province": "湖北"
        }
    }
}
 ```

- 使用uid 查询 pid - game_id 列表
 ```
 {
    "code": 0,
    "desc": "success",
    "result": {
        "1073491953_11346": {
            "player_id": 1073491953,
            "game_id": 11346
        },
        "1073491953_11074": {
            "player_id": 1073491953,
            "game_id": 11074
        }
    }
}
 ```

- 使用 token ,appkey 查询用户id
```
{
    "code": 0,
    "desc": "success",
    "result": {
        "player_id": "1455140931",
        "game_id": "10389",
        "openid": "1b613054bdd3c2eddf9ed88f813030e3"
    }
}
```

- 返回数据说明

|  名称 | 类型  | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| result | object  | 响应的数据，一般请求成功则不为空，其他为空 |
| player_id | object  | 业务级别用户id|
| game_id | int | 游戏id |
| openid | string | 帐号id |



## 5. 应用的token更换[/sns/oauth_token]
**简要描述：**
- IPG等服务端调用接口API
- 一个应用登录后，换取另一个应用的token 使用
- 需要配置IP白名单
**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/oauth_token
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ---- | ---- | ---- | ---- |
| token_key | int | Y | 登录返回的token_key |
| appkey | string | Y | 应用key |

- 响应结果
```
{
    "code": 0,
    "desc": "success",
    "result": {
        "token_key": "8982713bf5c995e2bca1a083eb4b24b405b51ad07",
        "token_secret": "b6daa0aecd59fcbb9716034ba7861119"
    }
}
```


## 6. 修改用户信息 [/sns/update_profile]
**简要描述：**
- 社区. 微信商城，IPG等服务端调用接口API
- 需要配置IP白名单
- 

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/update_profile
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ---- | ---- | ---- | ---- |
| uid | int | Y | 帐号id |
| nickname | string | N | 用户昵称 |
| avatar_url | string | N | 头像地址 |
| gender | string | N |   性别 |
| birthday| string | N | 生日 |
| password | string | N | 新密码 |
| old_password | string | N | 老密码 |


- 响应结果
```
{
    "code": 0,
    "desc": "success",
    "result": {
        "user_id": "3103351146",
        "nick_name": "test1111",
        "avatar_url": "http://test.ids111.com/11111/3103351146",
        "gender": "n",
        "birthday": "2018-1-1"
    }
}
```

## 7. openAPI 替代方案 [/sns/plugin]
**简要描述：**
- 社区. 微信商城，IPG等服务端调用接口API
- 需要配置IP白名单
- 使用token 查询玩家id(player_id),游戏id(game_id),用户id(uid)，uid 有可能为空

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/plugin
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| token | string | Y | 登录返回的登录票据 |
| auth_game_type | string | Y | 游戏类型（1:网游；2：休闲） |

 **响应结果**
 ```
 {
    "code": 0,
    "desc": "success",
    "result": {
        "player_id": "3103349746",
        "game_id": "10389",
        "uid": ""
    }
}
 ```


## 8. 手机号的解绑（业务级别） [/account/unBind]
**简要描述：**
- 需要配置IP白名单

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/account/unBind
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| player_id | string | Y | 业务级别的pid |
| appkey | string | Y | 应用appkey |
| mobile | string | Y | 手机号 |
| auth_game_type | string | Y | 游戏类型，1为网游；2为休闲；|
| sign | string | N | 签名规则参考（[签名规则](http://dc.idreamsky.com/tongyizhanghaoxiangguanapijiek/show/140.html#h2--sign- "签名规则")） |

 **响应结果**
 ```
 {
    "code": 0,
    "desc": "success",
    "result": {
        "pid": "3103350990",
        "uid": "3103350991",
    }
}
 ```

## 9. 更换手机号 [/sns/change_phone]
**简要描述：**
- 需要配置IP白名单
- 客服系统调用

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/change_phone
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| uid | string | Y | 需要更换手机号的帐号 |
| code | int | Y | 验证码 |
| mobile | string | Y | 手机号 |

 **响应结果**
 ```
{
    "code": 0,
    "desc": "success",
    "result": {
        "uid": "3103350991"
    }
}
 ```
## 9. 获取验证码接口 [/sns/getcode]
**简要描述：**
- 需要配置IP白名单
- 客服系统调用

**请求URL：** 
- [域名](http://gwiki.idreamsky.com/zhanghaotongyiyewuceng/show/564.html#h2-u57DFu540D)

- ` http://xx.com/sns/getcode
  
**请求方式：**
- POST 

**请求参数：** 

|  名称 | 类型  |  必须 | 描述  |
| ------------ | ------------ | ------------ | ------------ |
| mobile | string | Y | 手机号 |
| type|是  |string |短信验证码类型（login：登录；resetpasswd：重置密码； replace：换绑；|


 **响应结果**
 ```
{
    "code": 0,
    "desc": "success",
    "result": {
        "code": "9341"
    }
}
 ```

## 附录1. 签名[sign]

- 说明
> 每个应用需要独立申请应用数据，申请方式与游戏相同

- 签名方法
> 1. 将请求的参数按照 ASCII 的顺序进行排序，按照key=vaule,ping接键值对,并用 '&' 符号进行连接
2. 将第一步的值ping接 应用秘钥  得到签名源串
3. 将签名源串进行MD5 加密得到得到签名值

- 参考实例（登录接口为例）
```
1. 某应用参数如下
appkey  : ed2dfbf491e009e2dc71a37ac03f5
appsecure : 70160d9df66cc8a1a98db8eab21d667905b4d864e
2. 登录参数为
login_name:15817482390
appkey:7dfed2dfbf491e009e2dc71a37ac03f5
code:RTRE
sign:523626b329ce13f454f39e6bcc27f62f
grant_type:authorization_code
```
> 1. 将请求的参数按照 ASCII 的顺序进行排序，按照key=vaule,ping接键值对,并用 '&' 符号进行连接； `appkey=7dfed2dfbf491e009e2dc71a37ac03f5&code=RTRE&grant_type=authorization_code&login_name=15817482390`
2. 将第一步的值ping接 应用秘钥 得到签名源串 str： `appkey=7dfed2dfbf491e009e2dc71a37ac03f5&code=RTRE&grant_type=authorization_code&login_name=15817482390&70160d9df66cc8a1a98db8eab21d667905b4d864e`
3. 将签名源串进行MD5 加密得到得到签名值：`MD5(str)得到523626b329ce13f454f39e6bcc27f62f`

## 附录2. 公共错误码
<table cellspacing="0">
	<tbody>
		<tr>
			<td><strong>错误码(code)</strong></td>
			<td><strong>key</strong></td>
			<td><strong>说明</strong></td>
			<td><strong>描述</strong></td>
		</tr>
		<tr>
			<td>0</td>
			<td>success</td>
			<td>成功 非0代表异常</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>1</td>
			<td>&nbsp;</td>
			<td>请选择的帐号登录</td>
			<td>当前设备已绑定过手机号，但token失效</td>
		</tr>
		<tr>
			<td>1000~1999</td>
			<td>&nbsp;</td>
			<td>api响应类</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>1000</td>
			<td>&nbsp;</td>
			<td>会话已过期，请重新登录</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>1100</td>
			<td>&nbsp;</td>
			<td>登录失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>1101</td>
			<td>&nbsp;</td>
			<td>API请求失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>1108</td>
			<td>&nbsp;</td>
			<td>登录验证失败</td>
			<td>请求第三方帐号验证失败</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2001</td>
			<td>&nbsp;</td>
			<td>用户名密码错误</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2002</td>
			<td>&nbsp;</td>
			<td>修改密码失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2003</td>
			<td>&nbsp;</td>
			<td>更新个人信息失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2004</td>
			<td>&nbsp;</td>
			<td>创建用户失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2005</td>
			<td>&nbsp;</td>
			<td>用户已绑定手机</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2006</td>
			<td>&nbsp;</td>
			<td>该手机号已被绑定</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2007</td>
			<td>&nbsp;</td>
			<td>手机号不存在</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2008</td>
			<td>&nbsp;</td>
			<td>绑定失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2009</td>
			<td>&nbsp;</td>
			<td>更换手机失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2010</td>
			<td>&nbsp;</td>
			<td>用户未绑定手机</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2011</td>
			<td>&nbsp;</td>
			<td>发送短信验证码失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2012</td>
			<td>&nbsp;</td>
			<td>验证码无效</td>
			<td>验证码发送的手机和上传的手机号不匹配</td>
		</tr>
		<tr>
			<td>2013</td>
			<td>&nbsp;</td>
			<td>验证码错误</td>
			<td>验证码不存在、录入错误或过期（5分钟时效）</td>
		</tr>
		<tr>
			<td>2014</td>
			<td>&nbsp;</td>
			<td>该手机今日验证码请求次数已超出限制</td>
			<td>10次每日</td>
		</tr>
		<tr>
			<td>2017</td>
			<td>&nbsp;</td>
			<td>证件号不正确</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2018</td>
			<td>&nbsp;</td>
			<td>帐号已通过实名认证</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2019</td>
			<td>&nbsp;</td>
			<td>认证失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2020</td>
			<td>&nbsp;</td>
			<td>请绑定手机号后继续</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2021</td>
			<td>&nbsp;</td>
			<td>该手机号已被注册</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2022</td>
			<td>&nbsp;</td>
			<td>不允许更换token</td>
			<td>不允许非平台帐号登录令牌换取其他应用登录令牌</td>
		</tr>
		<tr>
			<td>2023</td>
			<td>&nbsp;</td>
			<td>第三方帐号绑定失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2024</td>
			<td>&nbsp;</td>
			<td>今日换设备绑定/登录次数已达到上限</td>
			<td>业务级限制</td>
		</tr>
		<tr>
			<td>2025</td>
			<td>&nbsp;</td>
			<td>今日更换手机号次数已达到上限</td>
			<td>业务级限制</td>
		</tr>
		<tr>
			<td>2026</td>
			<td>&nbsp;</td>
			<td>旧密码错误</td>
			<td>修改密码</td>
		</tr>
		<tr>
			<td>2027</td>
			<td>&nbsp;</td>
			<td>解绑失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>2999</td>
			<td>&nbsp;</td>
			<td>签名校验失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3000~3999</td>
			<td>&nbsp;</td>
			<td>参数类</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3001</td>
			<td>&nbsp;</td>
			<td>缺少必要参数或参数无效</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3002</td>
			<td>&nbsp;</td>
			<td>请输入旧密码</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3100</td>
			<td>&nbsp;</td>
			<td>手机格式不符</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3101</td>
			<td>&nbsp;</td>
			<td>邮箱格式不符</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3102</td>
			<td>&nbsp;</td>
			<td>密码格式不符</td>
			<td>6-20位字母、数字或符号组成</td>
		</tr>
		<tr>
			<td>3104</td>
			<td>&nbsp;</td>
			<td>配置数据获取失败</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3900</td>
			<td>&nbsp;</td>
			<td>invalid consumer key</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>3901</td>
			<td>&nbsp;</td>
			<td>token_key empty</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>9000~9999</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>9000</td>
			<td>Forbidden</td>
			<td>拒绝访问</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>9001</td>
			<td>&nbsp;</td>
			<td>请求方式错误</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>9999</td>
			<td>&nbsp;</td>
			<td>系统内部错误</td>
			<td>&nbsp;</td>
		</tr>
	</tbody>
</table>



