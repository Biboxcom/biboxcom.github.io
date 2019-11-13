# 现货API列表

## Market
> 市场行情

## Spot
> 现货交易

## Credit
> 信用交易

{% method %}
#### 系统剩余可借
> 获取闪借中系统剩余可借数量

- path: ** /v1/credit **
- method: ** POST **

| 参数名称        | 是否必须 | 类型   | 描述 | 默认值  | 取值范围 |
| ----------- | ---- | ---- | ------------ | ---- | ---- |
| coin_symbol     | true  | string |  交易币种   |       |  USDT, EOS, ...        |
| amount     | true  | double |  放款数量   |       |          |
| interest_rate     | true  | double |  放款利率   |       |      |
| is_insurance     | true  | integer |  是否开启保险   |       |  0或1    |
| force     | true  | integer |     |       |   1   |

{% sample lang="js" %}
请求:
```js
{
    "cmd": "borrowOrder/systemLeft", 
    "body": {}
}
```

{% sample lang="python" %}
请求:
```python
{
    "cmd": "borrowOrder/systemLeft", 
    "body": {}
}
```

{% common %}
返回:
```js
{
    "result": [
        {
            "result": [
                {
                    "coin_symbol": "BTC",
                    "config_interest_rate": 0.0001,
                    "lendcan": 0
                },
                {
                    "coin_symbol": "ETH",
                    "config_interest_rate": 0.0001,
                    "lendcan": 0
                },
                {
                    "coin_symbol": "USDT",
                    "config_interest_rate": 0.0001,
                    "lendcan": 0
                }
            ],
            "cmd": "borrowOrder/systemLeft"
        }
    ]
}
```

{% endmethod %}
