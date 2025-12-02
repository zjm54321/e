
====================

本项目使用 `uv` 管理依赖，在运行前需要先用 `uv sync` 同步依赖，然后**进入虚拟环境手动激活，再运行程序**。

环境要求
--------
- 已安装 Python（推荐 3.13 或 `pyproject.toml` 中指定的版本及以上）
- 已安装 `uv` 工具

安装 uv（如未安装）
--------------------
在 PowerShell 中执行：

```pwsh
python -m pip install uv
```

使用 uv sync 安装依赖
----------------------
在项目根目录（包含 `pyproject.toml` 的目录）打开 PowerShell，执行：

```pwsh
uv sync
```

首次会创建虚拟环境并安装 `numpy`、`opencv-python` 等依赖。

激活虚拟环境并运行程序（PowerShell）
--------------------------------------
`uv sync` 完成后，`uv` 会在项目下创建一个虚拟环境（通常在 `.venv` 或 `.uv` 目录中）。

1. 在项目根目录下激活虚拟环境：

```pwsh
.\.venv\Scripts\Activate.ps1
```

> 注意：如果你的虚拟环境目录名不是 `.venv`，请根据实际目录名修改上面的路径。

2. 激活成功后，直接运行程序：

```pwsh
.\simulation.exe
```

调试输出
--------
- 程序启动后会在标准输出打印：`debug=true`、`task 1`、`LEFT` 等信息。
- 调试日志（带 `[Debug]` 前缀）会输出到 stderr，不影响 stdout 中的控制指令解析。


