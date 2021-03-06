# 创建账户接口
---
URL:{baseurl}/api
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "create_account1",
    "params": {
        "pwd": "hyf"
    }
}
```
## 下行
```json
{
    "id": 0,
    "jsonrpc": "2.0",
    "result": {
        "address": "0xe3A81Fc2C6d38763D2C167A602B1b540554f57F4",
        "keystore": {
            "address": "e3a81fc2c6d38763d2c167a602b1b540554f57f4",
            "crypto": {
                "cipher": "aes-128-ctr",
                "cipherparams": {
                    "iv": "75371729d87a56b9598c69533856a5d3"
                },
                "ciphertext": "2119778e59ab0191419c6134423241948e862a8b979258cfa73e4e61a83f2b79",
                "kdf": "pbkdf2",
                "kdfparams": {
                    "c": 1000000,
                    "dklen": 32,
                    "prf": "hmac-sha256",
                    "salt": "9acab82ebea752bf921cc408966e8b21"
                },
                "mac": "5593bf5c41bf9a3b9fb2ddc7764125b63739d5e39dd649d498444ec7c4c736d1"
            },
            "id": "b6875b47-0dca-457e-9d13-236e7a4f15bb",
            "version": 3
        }
    }
}
```
```
error
{'result': {'error': 'no password'}, 'id': 0, 'jsonrpc': '2.0'}
```
# 获取余额
---
URL:{baseurl}/api
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "get_balance",
    "params": {
        "account": "0xe3A81Fc2C6d38763D2C167A602B1b540554f57F4"
    }
}
```
## 下行
```json
{
    "id": 0,
    "jsonrpc": "2.0",
    "result": {
        "address": "0xe3A81Fc2C6d38763D2C167A602B1b540554f57F4",
        "keystore": {
            "address": "e3a81fc2c6d38763d2c167a602b1b540554f57f4",
            "eth_balance": 100
    }
}
```
```
error
{'result': {"error": "no account"}, 'id': 0, 'jsonrpc': '2.0'}
```
# 发送裸交易
---
URL:{baseurl}/api
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "send_transaction",
    "params": {
        "to_address": "0xe3A81Fc2C6d38763D2C167A602B1b540554f57F4",
        "value":10,
        "pwd":"xxxx",
        "keystore":{},
    }
}
```
## 下行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "tx_hash": "xxxxxx"
    }
}
```
```
error
{'result': {"error": "xx error"}, 'id': 0, 'jsonrpc': '2.0'}
```
# 导入私钥创建账户
---
URL:{baseurl}/api
## 上行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "import_private_key",
    "params": {
        "private_key": "xxxxx",
        "pwd": "xxx"
    }
}
```
## 下行
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "address": "xxxx",
        "keystore": {}
    }
}
```
```
error
{'result': {"error": "xx error"}, 'id': 0, 'jsonrpc': '2.0'}
```
# 导出私钥
---
URL:{baseurl}/api
## 上行
```
{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "import_private_key",
    "params": {
        "private_key": "xxxxx",
        "pwd": "xxx"
    }
}
```
## 下行
```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "private_key": "xxxx"
    }
}
```
```
error
{'result': {"error": "xx error"}, 'id': 0, 'jsonrpc': '2.0'}
```
