# ZERO·R

> **面向智能驾驶场景的自主智能系统**

ZERO·R 是一个面向智能驾驶与机器人方向的开源实践项目，基于智能驾驶小车平台进行开发，探索感知、决策、规划与车辆控制等技术在实际移动机器人场景中的应用。

项目以工程实践为核心，从底层车辆通信与控制出发，逐步构建完整的自主驾驶系统。

---

## 🚗 项目简介

ZERO·R 致力于构建一个具备环境感知、自主决策与运动控制能力的智能驾驶系统。

项目当前基于 **Cyber 自动驾驶智能车**进行开发，并围绕实际比赛与实验场景逐步实现：

* 环境感知
* 目标与道路识别
* 自主导航
* 路径规划
* 行为决策
* 车辆运动控制
* 智能驾驶系统通信

项目不会将所有功能集中在单一程序中，而是采用模块化架构，将感知、决策、规划、控制与通信进行解耦。

---

## 🎯 项目目标

ZERO·R 的开发目标是逐步建立一套完整的智能驾驶系统：

```text
        ┌──────────────┐
        │   Sensors    │
        │ 摄像头 / 传感器 │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │  Perception  │
        │     感知      │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │   Decision   │
        │     决策      │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │   Planning   │
        │     规划      │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │   Control    │
        │     控制      │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │    Vehicle   │
        │     车辆      │
        └──────────────┘
```

最终形成从：

**感知 → 决策 → 规划 → 控制 → 执行**

的完整闭环。

---

## 🧩 项目架构

项目采用 Python `src` Layout，并按照智能驾驶系统中的功能职责进行模块划分。

```text
ZERO_R/
│
├── src/
│   └── zero_r/
│       ├── perception/       # 环境感知
│       ├── planning/         # 路径规划
│       ├── control/          # 车辆控制
│       ├── decision/         # 行为决策
│       ├── communication/    # 系统通信
│       ├── common/           # 公共模块
│       └── main.py           # 系统入口
│
├── tests/                    # 自动化测试
├── configs/                  # 系统配置
├── scripts/                  # 启动与辅助脚本
├── models/                   # AI 模型
├── data/                     # 数据与实验数据
├── docs/                     # 项目文档
│
├── requirements.txt          # Python 依赖
├── pyproject.toml            # Python 项目配置
├── README.md
├── LICENSE
└── .gitignore
```

---

## 🛠️ 技术栈

项目技术栈将根据实际开发阶段逐步引入。

### 当前基础环境

* Python 3.11
* Git
* GitHub
* `venv`
* setuptools

### 计划使用

* ROS
* Apollo 自动驾驶框架
* OpenCV
* NumPy
* AI / Computer Vision
* 路径规划与车辆控制

> 部分技术目前处于开发与验证阶段，具体版本及依赖关系以项目实际代码为准。

---

## 💻 开发环境

当前项目使用：

```text
Python 3.11.x
```

创建虚拟环境：

```bash
python3.11 -m venv .venv
```

激活环境：

### macOS / Linux

```bash
source .venv/bin/activate
```

### Windows

```powershell
.venv\Scripts\activate
```

安装项目：

```bash
python -m pip install -e .
```

---

## ▶️ 运行项目

激活虚拟环境后：

```bash
python -m zero_r.main
```

当前程序用于验证项目基础运行环境。

随着系统功能逐步开发，具体启动方式将根据 ROS / Apollo 等运行环境进行调整。

---

## 🧪 测试

项目使用独立的 `tests/` 目录进行功能测试。

运行测试：

```bash
python -m pytest
```

测试内容将覆盖：

* 感知模块
* 决策逻辑
* 路径规划
* 控制逻辑
* 通信接口
* 核心工具模块

---

## 📁 数据与模型

实验数据存放于：

```text
data/
```

AI 模型存放于：

```text
models/
```

大型模型文件、原始数据集以及其他不适合直接提交到 Git 仓库的文件，不直接纳入版本控制。

---

## 🔀 Git 工作流

项目采用 Git 进行版本控制。

推荐提交格式：

```text
feat: 新增功能
fix: 修复问题
refactor: 重构代码
docs: 更新文档
test: 添加测试
chore: 项目配置
```

例如：

```bash
git add .
git commit -m "feat: add object detection module"
git push
```

---

## 📌 开发状态

> **Project Status: Early Development**

当前阶段主要完成：

* [x] Git 仓库初始化
* [x] Python 3.11 开发环境
* [x] Python `src` 项目结构
* [x] 基础运行入口
* [ ] 车辆通信
* [ ] ROS / Apollo 环境接入
* [ ] 摄像头数据接入
* [ ] 环境感知
* [ ] 目标识别
* [ ] 路径规划
* [ ] 行为决策
* [ ] 车辆控制
* [ ] 完整自动驾驶闭环

项目功能会随着开发进度持续更新。

---

## ⚠️ 项目说明

ZERO·R 是一个用于**学习、研究、实验与竞赛实践**的智能驾驶项目。

项目中的自动驾驶功能应在受控、封闭且符合安全要求的环境中进行测试。

未经充分验证的代码不得直接用于真实道路或其他可能危及人员安全的环境。

---

## 📜 License

本项目采用 **[LICENSE](LICENSE)** 中规定的许可协议。

未经项目维护者明确授权，不得对本项目进行复制、修改、二次开发、重新发布或将其用于商业用途。

具体权利与限制以 `LICENSE` 文件为准。

---

## 👥 Contributors

ZERO·R 由项目团队共同开发。

项目成员：

* **Waiting** — Project Lead / Software Development
* **Hi_Tao** — Perception / Visual Recognition
* **Xiang** — System Development / Collaboration

---

<p align="center">
  <b>ZERO·R</b>
  <br>
  Building intelligence for autonomous mobility.
</p>
