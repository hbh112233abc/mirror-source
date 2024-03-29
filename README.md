# 配置镜像源

> 快速设置国内镜像源,方便记不住源地址的小伙子

## 安装

```shell
pip install mirror-source
```

## 使用

```shell
python -m mirror_source
```

```shell

请选择要设置的镜像源

    [0] [清华](https://pypi.tuna.tsinghua.edu.cn/simple)

    [1] [阿里云](https://mirrors.aliyun.com/pypi/simple/)

    [2] [网易](https://mirrors.163.com/pypi/simple/)

    [3] [豆瓣](https://pypi.douban.com/simple/)

    [4] [百度云](https://mirror.baidu.com/pypi/simple/)

    [5] [华为云](https://mirrors.huaweicloud.com/repository/pypi/simple/)

    [6] [腾讯云](https://mirrors.cloud.tencent.com/pypi/simple/)

[Default:0]> 1
:) Success setting source: https://mirrors.aliyun.com/pypi/simple/
```

## 功能介绍

- Windows 环境配置`%APPDATA%/pip/pip.ini`

  ```ini
  [global]
  index-url = 镜像源URL
  [install]
  trusted-host = 镜像源域名
  ```

- Linux/Mac 环境配置`~/.pip/pip.conf`

  ```ini
  [global]
  index-url = 镜像源URL
  [install]
  trusted-host = 镜像源域名
  ```

- pipenv 环境配置`.Pipfile`

  ```toml
  [[source]]
  url = "镜像源URL"
  verify_ssl = true
  name = "镜像源域名"
  ```

- poetry 环境配置`pyproject.toml`

  ```toml
  [[tool.poetry.source]]
  name = "镜像源域名"
  url = "镜像源URL"
  default = true
  ```
