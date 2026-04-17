# 医疗纠纷社会工作案例系统

基于AI的医疗纠纷案例模拟与伦理教学平台

## 🎯 项目简介

这是一个交互式的社会工作案例教学系统，模拟真实的骨科病房医患冲突场景，帮助使用者：
- 体验医务社工的真实工作情境
- 学习危机干预技巧
- 理解社会工作伦理原则
- 提升沟通与调解能力

## ✨ 核心功能

### 1. AI角色扮演
- **张女士**（患者）：情绪激动，感到被背叛
- **王先生**（家属）：愤怒且保护欲强
- **李主任**（医生）：专业但焦虑
- **刘护士长**（护士）：温和善解人意

### 2. 实时伦理分析
- 立场倾向检测（偏向院方/患者/中立）
- 共情能力评估
- 专业度评分
- 改进建议生成

### 3. 案例推进系统
- 8个关键节点
- 动态情节发展
- 自然过渡叙述
- 多角色切换

## 🚀 快速开始

### 本地开发

```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 访问 http://localhost:5173
```

### 生产构建

```bash
# 构建生产版本
npm run build

# 预览构建结果
npm run preview
```

## ⚙️ 配置说明

### API密钥配置（可选）

系统已内置默认API密钥，可以直接使用。如需自定义：

1. 复制环境变量模板：
```bash
cp .env.example .env.local
```

2. 编辑 `.env.local`：
```env
VITE_DEEPSEEK_API_KEY=your_api_key_here
VITE_DEEPSEEK_API_URL=https://api.deepseek.com/chat/completions
```

> **注意：** `.env.local` 文件已被 `.gitignore` 忽略，不会上传到GitHub。

## 📦 GitHub Pages部署

本项目已配置为支持GitHub Pages部署到子路径 `/Medical_Complaints/`。

### 自动部署（推荐）

使用GitHub Actions自动部署：

1. Fork或Clone本仓库
2. 进入仓库 Settings → Pages
3. Source选择 `GitHub Actions`
4. 选择 "Deploy to GitHub Pages" 工作流
5. 每次推送代码会自动部署

### 手动部署

```bash
# 构建项目
npm run build

# 进入dist目录
cd dist

# 初始化Git仓库
git init
git add -A
git commit -m 'deploy'

# 推送到gh-pages分支
git push -f git@github.com:youzhen1545/Medical_Complaints.git main:gh-pages
```

访问：https://youzhen1545.github.io/Medical_Complaints/

## 🎮 使用指南

1. **进入首页**：阅读案例背景和交互规则
2. **开始案例**：点击"开始案例"按钮
3. **角色扮演**：作为社工小李，与AI角色对话
4. **查看反馈**：每轮对话后查看伦理分析面板
5. **推进情节**：根据你的决策，案例会动态发展

## 💡 最佳实践

### 作为社工，你应该：

✅ **保持价值中立**
- 不偏袒任何一方
- 理解各方的立场和感受

✅ **运用积极倾听**
- 认真倾听对方的诉求
- 反馈你的理解

✅ **展现共情能力**
- 表达理解和关心
- 认可对方的情感

✅ **提供专业建议**
- 引导通过正规渠道解决
- 建议第三方鉴定

### 应该避免：

❌ 过早下结论
❌ 否定对方的感受
❌ 站在某一方的立场辩护
❌ 给出不切实际的承诺

## 🔧 技术栈

- **前端框架**: React 19
- **构建工具**: Vite 8
- **AI引擎**: DeepSeek API
- **图标库**: Lucide React
- **路由**: React Router DOM

## 📁 项目结构

```
src/
├── pages/
│   ├── HomePage.jsx          # 首页组件（含CSS）
│   └── SimulationPage.jsx    # 模拟对话页面（含数据+CSS）
├── services/
│   └── deepseek.js           # DeepSeek API服务
├── App.jsx                   # 路由配置
├── App.css                   # 全局样式
└── main.jsx                  # 应用入口
```

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交Issue和Pull Request！

## 📞 支持

如有问题，请提交GitHub Issue。

---

**开发者**: Social Work Education Team  
**版本**: 1.0.0  
**最后更新**: 2026-04-16
