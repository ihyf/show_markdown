# 获取支付宝url接口
---
URL:{baseurl}/hollywant/pay
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "call",
    "params": {
        "method": "pay_qrcode",
        "user_id": "16dc3a81e8ed9f7ec36398e84223f6a5",
        "account_id": "c76144252415e26839445c8ea141d4b3",
        "payment_type": "alipay",
        "payment_order": {
            "order_id": "7",
            "total_amount": 102
        }
    }
}
```
## 下行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "result": "success",
        "code_url": "https://qr.alipay.com/bax08035f5l0ycdsysvw00e8"
    }
}
```
# 支付宝订单查询
---
URL:{baseurl}/hollywant/pay
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "call",
    "params": {
        "method": "query_order",
        "payment_type": "alipay",
        "order_id": "6"
    }
}
```
## 下行
```json
{
    "jsonrpc": "2.0",
    "id": 111111,
    "result": {
        "msg": "SUCCESS",
        "title": "支付信息查询"
    }
}
```
# 获取微信url接口
---
URL:{baseurl}/hollywant/pay
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "call",
    "params": {
        "method": "pay_qrcode",
        "user_id": "16dc3a81e8ed9f7ec36398e84223f6a5",
        "account_id": "b8c0b4e4f7d33a51865adadca2aa2e7e",
        "payment_type": "weixin",
        "payment_order": {
            "order_id": "322-23zz2",
            "total_amount": 1
        }
    }
}
```
## 下行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "deviceInfo": "WEB",
        "sign": "64FE4963BEEF47865DE90078F4468FAD",
        "prepayId": "wx201612081759341e656b29660157442122",
        "returnCode": "SUCCESS",
        "returnMsg": "OK",
        "nonceStr": "bvqgOSGjsyFpSXdOzrqlfaV3wOENBJFT",
        "resultCode": "SUCCESS",
        "tradeType": "NATIVE",
        "mchId": "1358277702",
        "appid": "wx75f891b249a24ff9",
        "codeUrl": "weixin://wxpay/bizpayurl?pr=hb6fmah"
    }
}
```
# 微信获取支付结果
---
URL:{baseurl}/hollywant/pay
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "call",
    "params": {
        "method": "query_order",
        "payment_type": "weixin",
        "order_id": "2"
    }
}
```
## 下行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "msg": "FAIL",
        "title": "支付信息查询"
    }
}
```
# 旺币获取url
---
URL:{baseurl}/hollywant/pay
## 上行
```
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "call",
    "params": {
        "method": "pay_qrcode",
        "user_id": "16dc3a81e8ed9f7ec36398e84223f6a5",
        "account_id": "fbc8dd24544efe440c4e281807ec58bd",
        "payment_type": "wangbipay",
        "payment_order": {
            "order_id": "120914560",
            "total_amount": 0.1
        }
    }
}
```
## 下行
```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "msg": "https://open.weixin.qq.com/connect/oauth2/authorize?appid=wx160b97fc7a08acc3&redirect_uri=http://www.hotkidclub.com/vmc/payment.html?pcode=5179728b-c969-416e-880c-4cc845bedbc5&response_type=code&scope=snsapi_base#wechat_redirect",
        "title": "旺币支付url"
    }
}
```
# 旺币支付查询
---
URL:{baseurl}/hollywant/pay
## 上行
```
{
    "jsonrpc": "2.0",
    "id": 111111,
    "method": "call",
    "params": {
        "method": "query_order",
        "payment_type": "wangbipay",
        "order_id": "12091549"
    }
}
```
## 下行
```
{
    "jsonrpc": "2.0",
    "id": 111111,
    "result": {
        "msg": "SUCCESS",
        "title": "支付信息查询"
    }
}
```
