# AIDD Knowledge Copilot

AIDD Knowledge Copilot 是一个面向 AI 药物发现（AI-driven Drug Discovery, AIDD）的本地知识问答网站。

它以 ChatGPT 风格的简洁聊天界面呈现，内置 AIDD 相关知识库，覆盖靶点发现、虚拟筛选、生成式分子设计、ADMET、AlphaFold、公共数据库、模型评估、监管质量和项目落地等主题。

## 在线使用

如果你将本项目部署到 GitHub Pages，用户可以直接访问网站，无需安装任何软件。

本地预览也很简单：双击 `index.html`，或在浏览器中打开它。

## 功能

- ChatGPT 风格的中间聊天交互
- 本地关键词匹配型 AIDD 知识问答
- 问答、学习路线、风险检查三种模式
- 内置 AIDD 知识库和来源链接
- 可新增、导入、导出本地知识库
- 无需后端、无需数据库、无需 API Key

## 知识范围

当前内置知识覆盖：

- AIDD 基础概念
- 靶点发现与可成药性
- ChEMBL、PubChem、BindingDB、Open Targets、UniProt、PDB、AlphaFold DB
- QSAR、GNN、DTI、scaffold split、适用域、不确定性
- 分子对接、虚拟筛选、AutoDock Vina
- 生成式分子设计、SELFIES、逆合成、可合成性
- ADMET、PBPK、多参数优化
- 药物重定位、知识图谱、RAG
- FDA/EMA 对 AI 药物研发的质量与监管关注

## 项目结构

```text
.
├── index.html              # 网站入口，适合 GitHub Pages 部署
├── outputs/
│   ├── aidd-chatbot.html   # 生成版本备份
│   └── 使用说明.md
├── work/                   # 临时检查脚本
├── README.md
├── LICENSE
├── CONTRIBUTING.md
└── .gitignore
```

## 部署到 GitHub Pages

1. 在 GitHub 创建一个新仓库。
2. 上传本项目所有文件。
3. 进入仓库的 `Settings`。
4. 找到 `Pages`。
5. Source 选择 `Deploy from a branch`。
6. Branch 选择 `main`，目录选择 `/root`。
7. 保存后等待 GitHub Pages 构建完成。

之后你会得到一个公开访问链接。

## 本地开发

这个项目目前是纯静态 HTML，不需要安装依赖。

如果你想用本地服务器预览，可以在项目根目录运行：

```bash
python -m http.server 8000
```

然后访问：

```text
http://localhost:8000
```

## 重要说明

当前版本是本地关键词匹配型 chatbot，不会自动调用在线大模型。它适合做 AIDD 入门知识库、论文笔记库、教学演示和项目原型。

如果要升级为真正的智能问答系统，可以进一步接入 RAG、向量数据库和 OpenAI API，让它基于 PDF、论文、Excel 和实验记录生成带来源引用的回答。

## 许可证

本项目使用 MIT License。你可以自由使用、修改、分发和二次开发，但请保留许可证声明。
