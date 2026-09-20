# Zero-R

> **Zero·R 智能驾驶系统**
>
> 基于百度 Apollo CyberRT 的小型智能驾驶系统

Zero-R 是面向智能驾驶场景开发的自主驾驶系统，基于 **百度 Apollo CyberRT** 框架进行开发，运行于阿克曼转向智能车平台。

项目围绕机器视觉、环境感知、决策规划与车辆控制展开，实现智能车在指定赛道环境下的自主驾驶，并完成红绿灯识别、自动起步、人行道礼让、限速标识识别与减速以及赛道自主行驶等任务。

## 项目目标

Zero-R 的目标是构建一个模块化、可扩展的智能驾驶软件系统，实现：

* 🚦 交通信号灯识别与自动起步
* 🚶 人行道及行人场景识别与礼让
* 🚧 限速标识识别与自动减速
* 🛣️ 赛道与道路环境感知
* 🧭 自主决策与路径规划
* 🎮 车辆运动控制
* ⚙️ 基于 CyberRT 的模块通信与系统调度

## 系统架构

```text
                    Zero-R
                      │
        ┌─────────────┴─────────────┐
        │                           │
      感知层                     CyberRT
        │                           │
 ┌──────┼──────┐                    │
 │      │      │                    │
红绿灯  行人   限速标识             │
 │      │      │                    │
 └──────┼──────┘                    │
        │                           │
        ▼                           │
      决策规划 ◄────────────────────┘
        │
        ▼
      车辆控制
        │
        ▼
    阿克曼转向底盘
```

## 核心技术

| 模块        | 技术                   |
| --------- | -------------------- |
| 自动驾驶框架    | Baidu Apollo CyberRT |
| 操作系统      | Ubuntu               |
| AI / 深度学习 | PyTorch              |
| 视觉感知      | OpenCV / 深度学习模型      |
| 通信机制      | CyberRT              |
| 车辆平台      | 阿克曼转向智能车             |
| 编程语言      | Python / C++         |

## 硬件平台

项目使用 **智联 Cyber 自动驾驶智能车**作为实验与比赛平台。

主要特征：

* 阿克曼转向结构
* Apollo CyberRT 自动驾驶框架
* 模块化结构设计
* 丰富的输入输出设备
* 面向算法训练、模型部署与智能驾驶应用开发

## 比赛任务

项目当前面向智能驾驶赛道进行开发，需要完成以下自主驾驶任务：

1. **绿灯自动起步**
2. **人行道礼让行人**
3. **限速路段减速行驶**
4. **赛道自主竞速**

比赛过程中车辆需要自主完成任务，选手不得操作遥控器。

## 项目结构

```text
Zero-R/
├── perception/          # 环境感知
├── localization/        # 定位
├── planning/             # 决策与路径规划
├── control/              # 车辆控制
├── cyber/                # CyberRT 相关模块
├── models/               # AI 模型
├── config/               # 配置文件
├── launch/               # 启动配置
├── scripts/              # 工具脚本
├── docs/                 # 项目文档
└── README.md
```

> 项目结构将随着开发进度持续调整。

## Development Status

🚧 **Under Development**

当前项目处于开发阶段。

* [ ] CyberRT 环境搭建
* [ ] 智能车底盘通信测试
* [ ] 摄像头数据接入
* [ ] 车道线 / 道路感知
* [ ] 红绿灯识别
* [ ] 人行道识别
* [ ] 限速标识识别
* [ ] 自动起步
* [ ] 自动停车与礼让
* [ ] 自动减速
* [ ] 路径规划
* [ ] 车辆控制
* [ ] 全流程自主驾驶
* [ ] 赛道测试与优化

## Project Vision

Zero-R 不仅面向当前智能驾驶竞赛进行开发，也希望通过模块化的软件架构，逐步构建一个具备感知、决策、规划与控制能力的自主驾驶系统。

> **Zero-R · From Perception to Autonomy.**

## License

**Copyright © 2026 Zero-R Team. All Rights Reserved.**

Zero-R is a proprietary software project.

Unless otherwise expressly authorized in writing by the copyright holders, no person or organization may:

* copy, reproduce, modify, adapt, or create derivative works from this project;
* use this project or any substantial portion of its source code for any project, product, competition, research, or commercial purpose;
* redistribute, publish, sublicense, or otherwise make the source code or modified versions available to third parties;
* use the project's source code, architecture, algorithms, documentation, or other original materials for secondary development.

The source code is provided for **reference and evaluation purposes only**. No rights or licenses are granted by merely viewing or accessing this repository.

Any unauthorized use, reproduction, modification, distribution, or secondary development may constitute an infringement of the applicable intellectual property rights.

### Third-Party Components

This project may incorporate or depend upon third-party software, frameworks, libraries, models, or other components. Such components remain subject to their respective licenses and terms.

This license applies **only to original materials created by the Zero-R Team** and does not supersede or restrict the rights granted by applicable third-party licenses.

For permissions beyond those expressly granted above, please contact the copyright holders.
