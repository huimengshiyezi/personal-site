# 个人站（personal-site）

> 葉子的个人网站：主页 + 工具聚合页。线上地址 <https://ai-huimengshiyezi.top>

## 结构

| 目录 | 作用 |
|---|---|
| `个人站/` | **源码**（唯一源）：`index.html` 单文件（含全部样式与脚本）＋ `tools/` 工具页 ＋ `images/` 作品图与二维码 |
| `_deploy/` | **部署产物**：与 `个人站/` 同名文件逐字节相同的副本，直接拖进 EdgeOne Pages 发布 |

## 本地预览

双击 `个人站/index.html` 即可（纯静态、无构建步骤）。

## 部署

1. 改 `个人站/` 里的文件
2. 同步到 `_deploy/`（两份必须一致）
3. 把 `_deploy/` 内容拖进 EdgeOne Pages 完成发布

## 说明

本仓库只含站点本体。建站方案、收入规划等个人文档与提示词词库**不在仓库内**。

## 许可

MIT © huimengshiyezi (AI绘梦师葉子)
