# HTTP

HTTP 是一个传入数据协议，兼容 HTTP 1.x 代理。

* 名称：http
* 类型：Inbound
* 配置：

```javascript
{
  "timeout": 0,
  "accounts": [
    {
      "user": "my-username",
      "pass": "my-password"
    }
  ]
}
```

其中：

* `timeout`: 从客户端读取数据的超时设置（秒），0 表示不限时。默认值为 300。
* `accounts` (V2Ray 2.44+): 一个数组，数组中每个元素为一个用户帐号，用户名由`user`指定，密码由`pass`指定。默认值为空。
  * 当 `accounts` 非空时，HTTP 代理将对传入连接进行 Basic Authentication 验证。
