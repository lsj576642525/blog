# HTTP状态码

* 1xx表示消息
* 2xx表示成功
* 3xx表示重定向
* 4xx表示客户端错误
* 5xx表示服务端错误

### 常见的状态码

* 200

  > 最喜欢见到的状态码，表示请求成功

* 301

  > 永久重定向

* 302

  > 临时重定向

* 304

  > 自上次请求，未修改的文件

* 400

  > 错误的请求

* 401

  > 未被授权，需要身份验证，常见例如token信息等等

* 403

  > 请求被拒绝

* 404

  > 资源缺失，接口不存在，或者请求的文件不存在等等

* 500

  > 服务器端的未知错误

* 502

  > 网关错误

* 503

  > 服务暂时无法使用

### HTTP状态码中301，302和307有什么区别

* 301，Moved Permanently。永久重定向，该操作比较危险，需要谨慎操作：如果设置了301，但是一段时间后又想取消，但是浏览器中已经有了缓存，还是会重定向。
* 302，Fount。临时重定向，但是会在重定向的时候改变method：把 POST 改成 GET，于是有了307。
* 307，Temporary Redirect。临时重定向，在重定向时不会改变method。

### HTTP状态码中502和504有什么区别

* 502，Bad Gateway The server was acting as a gateway or proxy and received an invalid response from the upstream server。收到了上游响应但无法解析。
* 504，Gateway Timeout The server was acting as a gateway or proxy and did not receive a timely response from the upstream server。上游响应超时。