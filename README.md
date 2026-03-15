# CSMAR SDK (macOS / Linux)

一个适用于 **macOS 和 Linux** 的 CSMAR Python SDK 整理版本。

由于 CSMAR 官方提供的 Python SDK 更偏向 **Windows 环境**，在 macOS / Linux 系统中使用时配置不够友好。本项目对 SDK 进行了整理，使其能够在 **跨平台 Python 环境中更方便地使用**。

该 SDK 的调用方式类似常见的数据接口库，例如：

* `pandas`
* `tushare`

适用于：

* 金融数据研究
* 量化投资研究
* 资产定价研究
* 金融机器学习

---

# 环境要求

推荐 Python 版本：

```
Python >= 3.6
```

支持系统：

* macOS
* Linux
* Windows（在官网上下载即可）

---

# 安装步骤

## 1 克隆仓库

```bash
git clone https://github.com/yourname/csmar-python-sdk.git
```

---

## 2 安装依赖

```bash
pip install -r requirements.txt
```

依赖包括：

* urllib3
* websocket-client
* pandas

---

## 3 安装 SDK

将 `csmarapi` 目录复制到 Python 的 `site-packages` 目录。

例如：

```
/usr/local/lib/python3.x/site-packages/
```

或

```
/opt/homebrew/lib/python3.x/site-packages/
```

安装完成后的结构类似：

```
site-packages
 ├── pandas
 ├── numpy
 ├── csmarapi
```

---

# 使用示例

```python
import csmarapi

api = csmarapi.CsmarApi()

# 登录
api.login(
    username="your_account",
    password="your_password"
)

# 查询数据
data = api.query("STK_LISTEDCOINFO")

print(data.head())
```
---

# 常见用途

CSMAR 数据常用于：

* A股公司财务数据研究
* 因子投资研究
* 资产定价研究
* 宏观金融研究
* 金融机器学习

---

# 免责声明

本仓库仅用于 **CSMAR Python SDK 的整理与使用示例**。

本项目 **不包含任何 CSMAR 数据**。

使用 CSMAR 数据需拥有 **合法账号及数据库权限**。


