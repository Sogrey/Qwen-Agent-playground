# Qwen-Agent Playground 项目

## 项目概述

这是一个集成Qwen-Agent的开发环境，用于构建和测试基于通义千问大语言模型的智能体应用。项目通过git submodule方式集成了[Qwen-Agent](https://github.com/QwenLM/Qwen-Agent)框架。

## 主要组件

1. **Qwen-Agent核心框架** (qwen_agent目录)
   - 多智能体协作系统
   - 工具调用接口
   - 记忆管理模块
   - 对话管理引擎

2. **开发工具和示例**
   - 浏览器交互界面 (browser_qwen)
   - 测试套件 (tests)
   - 示例代码 (examples)

## 项目结构

```
Qwen-Agent-playground/
├── qwen_agent/            # Qwen-Agent子模块
│   ├── agents/            # 智能体实现
│   ├── tools/             # 工具库
│   ├── llm/               # 语言模型接口
│   ├── memory/            # 记忆管理
│   ├── examples/          # 示例代码
│   └── tests/             # 测试代码
├── README.md              # 项目文档
└── (其他项目文件)
```

## 快速开始

1. 初始化项目：
```bash
git submodule update --init --recursive
cd qwen_agent
pip install -r requirements.txt
```

2. 运行Web界面：
```bash
python browser_qwen/src/main.py
```

3. 或运行命令行示例：
```bash
python examples/demo.py
```

## 开发指南

- 添加新智能体：在`qwen_agent/agents/`中创建新模块
- 添加新工具：在`qwen_agent/tools/`中实现工具类
- 测试：使用`pytest tests/`运行测试

## 许可证

遵循Qwen-Agent的原始许可证(MIT License)。