# 👨‍🍳 callbaker

[![Download Callbaker](https://img.shields.io/pypi/v/callbaker.svg)](https://pypi.python.org/pypi/callbaker)
![CodeQL](https://github.com/torrua/callbaker/workflows/CodeQL/badge.svg?branch=master)
[![Build Status](https://travis-ci.com/torrua/callbaker.svg?branch=master)](https://travis-ci.com/torrua/callbaker)
[![codecov](https://codecov.io/gh/torrua/callbaker/branch/master/graph/badge.svg?token=CHCS5JEGZI)](https://codecov.io/gh/torrua/callbaker)

Telegram callback queries converter

## What it is

This tiny package can help you parse the callback data request response for telegram bots.

## How to install

``pip install callbaker``

## How to use

There are two main functions that might be helpfull for you:
`info_from_callback` get callback string and convert it to dict.
`callback_from_info` combine dict into string prepared for callback.

Examples:

```
result = callback_from_info(info={"k1": "str", "k2": 2, "k3": None, "k4": False, "k5": (1, 2)})
print(result)
```
```"&k1=str&k2=2&k3=None&k4=False&k5=(1, 2)"```


```
result = info_from_callback(call_data="&key_1=value_1&key_2=value_2")
print(result)
```
```{'key_1': 'value_1', 'key_2': 'value_2'}```
