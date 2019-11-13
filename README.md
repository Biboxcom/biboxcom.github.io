## Setup

```sh
sudo npm install -g gitbook-cli  # 全局安装cli

cd /path/of/gitbook

gitbook install ./  # 安装插件
gitbook serve  # 启动服务
```

## 生成静态HTML 
> 在_book目录下

## github page 上传

> gitboook 默认index.html 为语言选择页, 在上传静态文件到github page时, 可以替换/index.html 为下面内容重定向.

``` html
<!DOCTYPE HTML>
<html>
    <head>
        <title>Bibox API</title>
        <meta http-equiv="refresh" content="0; url=../zh-hans" />
    </head>
</html>
```

## 插件调整
i18n: 图标显示在右边