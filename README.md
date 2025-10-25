# VibeWithMe - 通用项目开发文档模板

本目录包含一套**与技术栈无关、为人类与AI协同开发设计**的项目开发文档模板。适用于各类项目：
- Tauri 桌面应用
- Next.js 前端
- FastAPI 后端
- uni-app 跨平台
- Python 数据挖掘
- 其他技术栈

## 核心理念

**文档驱动的AI协同开发**：
- 🎯 人类提出清晰需求，AI通过文档理解和执行
- 🤖 最小化上下文，让AI专注核心任务
- 📝 结构化信息便于AI处理
- 🔄 迭代优化，每阶段都有明确的验收标准

## 核心工作流程

```
用户故事
    ↓ (需求明确)
产品设计文档
    ↓ (方案定案)
Sprint规划
    ↓ (任务分解)
开发排期
    ↓ (优先级确定)
AI执行开发
    ↓ (代码交付)
验收&优化
    ↓ (问题反馈)
迭代下一Sprint
```

## 文档结构

```
project-docs/
├── 00_PROJECT_OVERVIEW/           # 项目概览（顶层）
│   ├── README.md                  # 项目总览
│   ├── ARCHITECTURE.md            # 架构设计
│   └── QUICK_START.md             # 快速开始
│
├── 01_VERSION_RELEASES/           # 版本发布文档
│   ├── vX.X.X/
│   │   ├── RELEASE_NOTES.md       # 发布说明
│   │   ├── USER_STORIES.md        # 用户故事（需求定义）
│   │   ├── DESIGN.md              # 产品设计文档
│   │   ├── IMPLEMENTATION_PLAN.md # Sprint规划和排期
│   │   └── LESSONS_LEARNED.md     # 经验教训
│
├── 02_TECHNICAL_GUIDES/           # 技术指南
│   ├── architecture/              # 架构相关
│   ├── database/                  # 数据库相关
│   └── modules/                   # 核心模块
│
├── 03_DEVELOPMENT_PROCESS/        # 开发流程
│   ├── AGILE_WORKFLOW.md          # 人类与AI协同工作流
│   ├── GIT_WORKFLOW.md            # Git分支策略
│   └── FEATURE_TEMPLATE.md        # 功能开发模板
│
├── 04_BUILD_DEPLOY/               # 构建和部署
│   ├── BUILD_GUIDE.md             # 构建指南
│   ├── DEPLOYMENT.md              # 部署流程
│   └── TESTING_CHECKLIST.md       # 测试清单
│
├── 05_TROUBLESHOOTING/            # 问题排查
│   ├── COMMON_ISSUES.md           # 常见问题FAQ
│   └── CRITICAL_FIXES/            # 问题记录
│
└── 06_ARCHIVE/                    # 归档文档
     └── deprecated/
```

## 快速开始

### 1. 复制模板
```bash
# 复制整个模板到你的项目
cp -r dev-template/ your-project/meta/
```

### 2. 自定义配置
编辑各文件中的占位符（如项目名称、技术栈等）

### 3. 关键文档说明

| 文档 | 用途 | 更新频率 | 更新者 |
|------|------|---------|--------|
| ARCHITECTURE.md | 架构设计、模块关系 | 每个版本 | 人类 |
| AGILE_WORKFLOW.md | 人类与AI协同工作流 | 项目初期 | 人类 |
| USER_STORIES.md | 需求定义 | 版本启动时 | 人类 |
| DESIGN.md | 产品设计 | 版本设计时 | 人类+AI |
| IMPLEMENTATION_PLAN.md | 任务排期 | Sprint开始 | 人类(优先级)+AI(分解) |
| PROGRESS_REPORT.md | 开发进度 | 每天 | AI |
| ISSUES.md | 问题跟踪 | 发现问题时 | AI(记录)+人类(决策) |
| LESSONS_LEARNED.md | 经验教训 | 版本完成后 | 人类 |

## 文档编写原则

### 1. 简洁直接
- 避免冗余描述
- 重点突出核心信息
- 代码示例简明扼要

### 2. AI友好
- 结构化信息便于AI理解
- 避免模糊表述
- 清晰的验收标准

### 3. 可执行性
- 提供具体的步骤
- 包含常见问题和解决方案
- 明确的成功标准

### 4. 不同技术栈的适配
- 架构章节可通用，只需调整模块名称
- 代码示例改为各自技术栈的语言
- 构建、部署命令完全替换
- 测试清单相同，测试工具不同

## 文档维护建议

### 项目启动
1. 完成 ARCHITECTURE.md（架构设计）
2. 制定 AGILE_WORKFLOW.md（工作流程）
3. 准备 QUICK_START.md（快速开始）

### 版本启动
1. 创建版本文件夹（如 v1.0.0/）
2. 编写 USER_STORIES.md（需求定义）
3. 编写 DESIGN.md（产品设计）
4. 制定 IMPLEMENTATION_PLAN.md（任务排期）

### 开发过程中
1. AI每天更新 PROGRESS_REPORT.md
2. 遇到问题立即记录在 ISSUES.md
3. 保存技术方案到 TECHNICAL_GUIDES/

### 版本完成后
1. 编写 LESSONS_LEARNED.md（经验教训）
2. 整合问题和解决方案
3. 编写 RELEASE_NOTES.md（发布说明）

## 典型项目的文档结构

### Tauri桌面应用
```
02_TECHNICAL_GUIDES/
├── frontend/          # Vue组件设计
├── backend/          # Rust后端服务
├── database/         # 本地SQLite
└── cross-platform/   # 跨平台构建
```

### Next.js前端项目
```
02_TECHNICAL_GUIDES/
├── frontend/         # React/Next.js组件
├── api-integration/  # 后端API集成
├── state-management/ # 状态管理
└── deployment/       # 部署配置
```

### FastAPI后端项目
```
02_TECHNICAL_GUIDES/
├── api-design/       # API规范
├── database/         # 数据模型
├── authentication/   # 认证机制
└── performance/      # 性能优化
```

### Python数据挖掘项目
```
02_TECHNICAL_GUIDES/
├── data-pipeline/    # 数据流程
├── analysis/         # 分析方法
├── visualization/    # 可视化
└── deployment/       # 模型部署
```

## 人类与AI协同的要点

### 人类职责
- ✅ 定义清晰的用户故事和需求
- ✅ 进行产品设计决策
- ✅ 确定任务优先级
- ✅ 验收和反馈
- ✅ 记录经验教训

### AI职责
- ✅ 理解并澄清需求
- ✅ 提出技术方案建议
- ✅ 分解任务
- ✅ 执行开发工作
- ✅ 维护进度报告
- ✅ 记录问题

### 协作要点
- 📝 **文档是沟通的纽带** - 清晰的文档让AI能准确执行
- 🎯 **明确的验收标准** - AI知道什么时候完成
- 🔄 **每日同步** - 10-20分钟的晚间反馈足够
- 📊 **进度透明** - AI每天更新进度报告

## 💎 三条金律

这是从 Nboost 开发中总结的最宝贵的经验：

1. **向后兼容 > 新功能**
   - 升级时保留用户数据比任何新功能都重要

2. **性能从设计开始**
   - 不是优化时才考虑性能，而是从架构设计开始

3. **需求清晰 > 代码速度**
   - 花时间做好需求分析，比快速编码更重要

## 🎓 适用项目类型

| 项目类型 | 适用度 | 为什么 |
|---------|--------|-------|
| 🖥️ Tauri桌面应用 | ⭐⭐⭐⭐⭐ | 直接来自 Nboost 经验 |
| 🌐 Next.js前端 | ⭐⭐⭐⭐⭐ | 通用敏捷流程完全适用 |
| 🔌 FastAPI后端 | ⭐⭐⭐⭐⭐ | 架构设计完全通用 |
| 📱 uni-app跨端 | ⭐⭐⭐⭐ | 需加强多端测试 |
| 🔬 Python数据挖掘 | ⭐⭐⭐⭐ | 需加强数据质量管理 |
| 👤 一个人项目 | ⭐⭐⭐⭐⭐ | 最佳使用场景 |
| 🏢 大型企业项目 | ⭐⭐⭐⭐ | 可进一步细化 |

## 关键文档深入说明

详见各模板文件：
- [AGILE_WORKFLOW.md](./01_AGILE_WORKFLOW.md) - 人类与AI协同工作流详解
- [IMPLEMENTATION_PLAN_TEMPLATE.md](./03_IMPLEMENTATION_PLAN_TEMPLATE.md) - 版本计划和排期模板
- [LESSONS_LEARNED_TEMPLATE.md](./04_LESSONS_LEARNED_TEMPLATE.md) - 经验教训模板
- [ARCHITECTURE_TEMPLATE.md](./02_ARCHITECTURE_TEMPLATE.md) - 架构设计模板

---

**版本**: v2.0 (为人类与AI协同设计，精简版)  
**最后更新**: 2025年10月  
**说明**: 合并了交付说明文档，保留核心内容，移除重复
