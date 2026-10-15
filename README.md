# Python 自动化单元测试

本项目演示使用 pytest 测试 Python 函数，并通过 GitHub Actions 在每次推送代码或创建、更新拉取请求时自动运行测试。

## 项目结构

```text
my-python-project/
├── .github/workflows/ci.yml
├── calculator.py
├── test_calculator.py
├── requirements.txt
└── README.md
```

## 本地运行

```bash
python -m pip install -r requirements.txt
python -m pytest -v
```

测试覆盖加法、负数相加、乘法和乘以零，正常输出为 `2 passed`。

## 查看自动测试结果

在 GitHub 仓库的 **Actions** 页面选择 **Python单元测试**，打开最近一次运行记录。

- 绿色对勾表示测试通过。
- 红色叉号表示运行失败，可展开“运行测试”步骤查看具体断言和错误信息。

工作流使用 Python 3.11，依赖版本由 `requirements.txt` 指定。
