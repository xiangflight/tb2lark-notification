# Connect Teambition and lark(飞书)
## 目标

将 teambition 的任务状态通知到 飞书 的自定义机器人中.

## 原理

飞书中, 每个群可以设置一个自定义机器人, 每个机器人有一个接收外部请求的 webhook url.

Teambition 中, 可以自定义企业内应用, 该应用可以向指定的 webhook url 推送企业内各项目任务的通知, 注意: 该应用需要被授予相应的权限.

## 实现

我们要做的就是 开发一个请求中转站, 处理 Teambition 发送过来的请求, 并将请求解析后, 发送给 飞书的群自定义机器人. 

依赖:

- Python3

- Flask, 参考 Flask 官网, 直接使用 `pip install Flask` 安装
- requests 库, 一个通用的 HTTP 库

运行:

```python
python webhook.py
```

如果要在生产环境部署, 参考 Flask 官方文档.