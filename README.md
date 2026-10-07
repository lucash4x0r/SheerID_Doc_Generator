# SheerID Doc Generator (身份验证文档生成器)

**Description**: 基于 React 构建的身份验证文档生成工具，支持学生和教师/职工文档模板，用于 UI 测试、验证流程开发和教育用途。

**🔗 Live Demo**: [https://acagen.suck-dick.tech/](https://acagen.suck-dick.tech/)

[English README](README_EN.md)

## 🌐 Deployment (部署指南)

推荐使用 **Cloudflare Pages** 进行免费托管。

1.  **Fork 本仓库**到你的 GitHub。
2.  登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)。
3.  进入 **Workers & Pages** -> **Create Application** -> **Pages** -> **Connect to Git**。
4.  选择你刚刚 Fork 的仓库。
5.  **构建设置 (Build settings)** (通常会自动检测):
    *   **Framework preset**: `Vite`
    *   **Build command**: `npm run build`
    *   **Build output directory**: `dist`
6.  **⚠️ 重要步骤**: 添加环境变量 (Environment Variables):
    *   `NPM_FLAGS` = `--legacy-peer-deps`
7.  点击 **Save and Deploy**。

### GitHub Pages（最简单）

本仓库已包含 `.github/workflows/deploy-pages.yml` 自动部署工作流。

1. 推送代码到 `main` 分支。
2. 进入 GitHub 仓库 **Settings** -> **Pages**。
3. 在 **Build and deployment** 中将 Source 设置为 **GitHub Actions**。
4. 等待工作流 **Deploy to GitHub Pages** 执行完成。
5. 访问线上地址：
   `https://<your-username>.github.io/SheerID_Doc_Generator/`

## 📖 简介 (Introduction)

这是一个基于 **React** + **Vite** + **HeroUI** 构建的现代化 Web 应用，用于快速生成身份验证文档模板。

### 学生文档 (Student Documents)
1.  **学费单 (Tuition Statement)**
2.  **成绩单 (Transcript)**
3.  **课程表 (Schedule)**
4.  **录取通知书 (Admission Letter)**
5.  **在读证明 (Enrollment Certificate)**
6.  **学生证 (Student ID Card)** - 正反面

### 教师/职工文档 (Teacher/Employee Documents)
7.  **雇佣信 (Employment Letter)**
8.  **工资单 (Salary Statement)**
9.  **教师证 (Teacher ID Card)** - 正反面
10. **教师资格证 (Teaching Certificate)**

支持一键随机生成仿真数据，自定义学校图标，并提供多种导出格式（单图拼接、ZIP打包）。

## ✨ 特性 (Features)

*   **现代化 UI**: 采用 [HeroUI (NextUI)](https://heroui.com) 构建，支持暗色模式，界面美观流畅。
*   **无限画布体验**: 采用 **Framer Motion** 构建的可拖拽、可缩放（Zoomable）无限画布，支持双视图切换（Standard/Extra）。
*   **一键生成**: 内置 Faker.js，可一键生成逼真的姓名、地址、日期、GPA、学分和课程信息。
*   **自定义校徽**: 支持上传自定义学校 Logo，实时更新到文档中。
*   **多种导出**:
    *   **Horizontal Stitch**: 将三份核心文档（学费/成绩/课表）横向拼接为一张长图。
    *   **Grid Stitch**: 网格拼接导出。
    *   **ZIP Archive**: 分别导出三张独立图片并打包为 ZIP。
    *   **独立文档下载**: 支持单独下载录取通知书和在读证明。
    *   **纯净导出**: 自动处理背景透明度，确保导出的图片背景纯白，无毛玻璃杂色。
*   **实时预览**: 所见即所得的文档预览效果。

## 🛠️ 技术栈 (Tech Stack)

*   [React](https://react.dev/)
*   [Vite](https://vitejs.dev/)
*   [Tailwind CSS](https://tailwindcss.com/)
*   [HeroUI](https://heroui.com/)
*   [html2canvas](https://html2canvas.hertzen.com/)
*   [Faker.js](https://fakerjs.dev/)

## 🚀 快速开始 (Quick Start)

1.  **安装依赖**
    ```bash
    npm install
    ```

2.  **启动开发服务器**
    ```bash
    npm run dev
    ```

3.  **构建生产版本**
    ```bash
    npm run build
    ```

## ⚠️ 免责声明 (Disclaimer)

**请在使用本软件前仔细阅读以下声明：**

1.  **仅供测试与教育用途**：本项目旨在为开发人员提供用于 UI 测试、布局验证及系统集成的测试数据生成工具。
2.  **严禁用于非法用途**：**严禁**使用本工具生成的文档进行任何形式的欺诈、伪造文件、身份冒充或绕过验证系统（如 SheerID、Unidays 等）。
3.  **无有效性**：本工具生成的文档均为虚构模版，不具备任何法律效力或官方认证效力。
4.  **免责条款**：作者不对任何人使用本软件产生的任何后果负责。使用本软件即表示您同意承担所有因使用该软件而产生的法律责任和风险。

**Please read carefully before using this software:**

This tool is intended for **educational and testing purposes only** (e.g., testing UI layouts, verifying upload flows). **DO NOT** use this tool to create fraudulent documents, misrepresent your identity, or bypass verification systems. The generated documents are fictitious and have no legal validity. The authors assume no liability for any misuse of this software.

## 📄 License

本项目采用 [MIT License](LICENSE) 开源，但使用需遵守上述免责声明。
