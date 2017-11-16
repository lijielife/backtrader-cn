## backtrader-cn

[![Build Status](https://travis-ci.org/pandalibin/backtrader-cn.svg?branch=master)](https://travis-ci.org/pandalibin/backtrader-cn)
[![Coverage Status](https://codecov.io/gh/pandalibin/backtrader-cn/branch/master/graph/badge.svg)](https://codecov.io/gh/pandalibin/backtrader-cn)
[![Doc Status](https://readthedocs.org/projects/backtrader-cn/badge/?version=latest)](http://backtrader-cn.readthedocs.io/en/latest/?badge=latest)

### 快速上手

python 版本

	$ python --version
	Python 3.6.0

注：

- 项目中使用了 `f-string`，所以，需要 `Python 3.6` 以上的版本。
- 可以使用 `pyenv` 安装不同版本的 `Python`，用 `pyenv virtualenv` 创建彼此独立的环境。

#### 下载代码

	$ git clone https://github.com/pandalibin/backtrader-cn.git

#### 安装 `mongodb`

##### Mac OSX

安装项目需要的软件包：

	$ brew install mongodb
	$ brew services start mongodb
	$ xcode-select --install  # 安装`arctic`模块报错提示缺少`limits.h`

##### Ubuntu/Debian

安装项目需要的软件包：

	$ sudo apt-get install gcc build-essential  # arctic
	$ sudo apt-get install mongodb

安装 Python modules

> ~~$ pip install -U -r requirements.txt~~

> `pip install -r requirements.txt` 会并行安装 Python modules。
>
> `tushare` 没有将它安装时依赖的包在 `setup.py` 的 `install_requires` 中做声明，导致如果在 `lxml` 安装之前安装 `tushare` 就会报错。

	$ make pip

获取股票数据

	$ python data_main.py

计算入场信号

	$ python frm_main.py
