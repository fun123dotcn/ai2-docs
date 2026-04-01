# App Inventor 2 中文文档

基于 [Mintlify](https://mintlify.com) 构建的 App Inventor 2 中文知识库。

## 🚀 快速开始

### 安装 Mintlify CLI

```bash
npm i -g mint
```

### 本地预览

```bash
cd ai2-docs
mint dev
```

访问 http://localhost:3000 预览文档。

### 部署到 GitHub Pages

本项目使用 GitHub Actions 自动部署。每次推送到 main 分支会自动构建并发布。

## 📁 项目结构

```
ai2-docs/
├── content/                    # 文档内容 (MDX格式)
│   ├── getting-started/       # 快速开始
│   ├── components/            # 组件参考
│   ├── extensions/            # 扩展中心
│   ├── tutorials/            # 教程
│   └── troubleshooting/       # 常见问题
├── public/                    # 静态资源
│   └── images/               # 图片
├── .github/
│   └── workflows/             # GitHub Actions
├── mint.json                  # Mintlify配置
└── README.md
```

## ✨ Mintlify 特性

- 📝 **MDX 支持** - 使用 Markdown + React 组件
- 🎨 **美观的 UI** - 开箱即用的现代设计
- 🌙 **深色模式** - 自动适配系统主题
- 🔍 **全文搜索** - 快速找到需要的内容
- 📱 **响应式设计** - 完美适配各种设备
- 🔗 **内置组件** - Accordion、Tabs、Card、CodeGroup 等

## 📖 如何贡献

1. Fork 本仓库
2. 创建新分支：`git checkout -b feature/new-tutorial`
3. 添加或修改文档（使用 MDX 格式）
4. 提交更改：`git commit -m 'Add new tutorial'`
5. 推送分支：`git push origin feature/new-tutorial`
6. 创建 Pull Request

## 📄 版权声明

本文档基于以下资源整理：

- [MIT App Inventor 官方文档](https://appinventor.mit.edu/reference/) (CC BY-SA 4.0)
- [MIT App Inventor Community](https://community.appinventor.mit.edu/)
- [MIT App Inventor GitHub](https://github.com/mit-cml/appinventor-sources)

所有内容版权归原作者所有。本文档由 ai2claw 整理，仅供学习参考。

## 🔗 相关链接

- [MIT App Inventor](https://appinventor.mit.edu/)
- [AI2 在线编辑器](https://ai2.appinventor.mit.edu/)
- [MIT App Inventor 社区](https://community.appinventor.mit.edu/)
- [官方扩展列表](https://mit-cml.github.io/extensions/)
- [Mintlify 文档](https://mintlify.com/docs)

---

Built with ❤️ by ai2claw 🐝
