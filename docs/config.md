本文将讲述说明一下js文件内各字段的用途。

js文件用来对vue-tcbj进行全局配置，指定后台错误返回码、微信公众号appId、是否启用微信的JSSDK能力 等。

以下是一个包含了部分配置选项的 tConfig.js：

```js
const config = {
  "appId": "wx88888888888",
  "openId": "43hjfvdoisu43j2khfsd",
  "baseURL": "https://www.domain.com",
  "isUseWxSdk": true,
  "publicPath": "https://www.domain.com/vue-tcbj/index.html",
  "wxSignatureApi": "/getJsSdkSignature",
  "wxAuthorizedApi": "/webDevAuthorized",
  "wxDebug": false,
  "wxJsApiList": [
        "hideOptionMenu",
        "scanQRCode"
  ],
  "errorCodeValue": "00",
  isCheckErrorCode:false
}

export default config
```

以下是tConfig.js 的配置项说明

### appId

###### string

指定了微信公众号appId，在获取openId 和 调用JSSDK能力时需要用到

### openId

###### string

默认为空。我们一般会在开发阶段指定一个默认的openId来调试

### baseURL

###### string

必填。服务器接口的域名地址

### isUseWxSdk

###### boolean

默认为 false。

是否调用JSSDK能力

### publicPath

###### string

静态文件发布后的路径

### wxSignatureApi

###### string

调用微信JSSDK的签名接口地址

### wxAuthorizedApi

###### string

获取openId的微信重定向接口

需要以 / 开头

### wxDebug

###### boolean

是否启用微信调试功能

### wxJsApiList

###### array

调用微信接口的列表

### errorCodeValue

###### string

默认为 00 

指定后台错误返回码

### isCheckErrorCode

###### boolean

是否检测errorCode并进行拦截
