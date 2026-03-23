# 部署到 GitHub Pages 指南

我已经为你准备好了所有文件，包括：
1. `lobster-investment-channel.html` - 主网页文件（原"小龙虾投资频道.html"）
2. `index.html` - 自动重定向首页
3. `README.md` - 项目说明文档
4. `deploy-to-github.md` - 本部署指南

文件已提交到本地 Git 仓库，你可以选择以下任一方法部署：

## 方法一：GitHub 网页上传（最简单）

1. **访问 GitHub**：打开 [github.com](https://github.com) 并登录
2. **创建仓库**：
   - 点击右上角 "+" → "New repository"
   - 名称：`lobster-investment-channel`（或自定义）
   - 描述：`小龙虾投资频道 - 专业交易分析网页`
   - 选择 **Public**（公开）
   - **不要**初始化 README、.gitignore 或许可证
   - 点击 "Create repository"

3. **上传文件**：
   - 在仓库页面，点击 "Add file" → "Upload files"
   - 将以下4个文件拖拽到上传区域：
     - `lobster-investment-channel.html`
     - `index.html`
     - `README.md`
     - `deploy-to-github.md`
   - 点击 "Commit changes"

4. **启用 GitHub Pages**：
   - 进入仓库 "Settings"（设置）
   - 左侧选择 "Pages"
   - "Source" 选择：`main` 分支，`/(root)` 文件夹
   - 点击 "Save"

## 方法二：命令行 Git（推荐）

如果你已安装 Git 并配置了 GitHub 账户：

```bash
# 1. 创建 GitHub 仓库（网页界面或 gh CLI）
# 2. 将本地仓库推送到 GitHub
git remote add origin https://github.com/YOUR_USERNAME/lobster-investment-channel.git
git push -u origin main

# 3. 启用 GitHub Pages（也可在网页设置）
gh repo edit --enable-pages  # 需要 GitHub CLI
```

## 方法三：GitHub Desktop

1. 下载并安装 [GitHub Desktop](https://desktop.github.com)
2. 登录你的 GitHub 账户
3. 选择 "Clone a repository" → "URL"
4. 粘贴仓库 URL
5. 将准备好的4个文件复制到仓库文件夹
6. 提交更改并推送

## 访问你的网站

部署后等待1-2分钟，访问：
- `https://YOUR_USERNAME.github.io/lobster-investment-channel/`（自动重定向）
- `https://YOUR_USERNAME.github.io/lobster-investment-channel/lobster-investment-channel.html`（直接访问）

## 快速测试（本地）

```bash
# 在包含这些文件的目录运行
python3 -m http.server 8000
# 然后在浏览器访问 http://localhost:8000
```

## 文件说明

- `lobster-investment-channel.html` - 主投资交易页面
- `index.html` - 自动重定向到主页面
- `README.md` - 项目文档
- `deploy-to-github.md` - 本部署指南

## 需要帮助？

如果你遇到问题：
1. 确保仓库名称为英文，没有特殊字符
2. GitHub Pages 需要几分钟才能生效
3. 检查浏览器控制台是否有错误
4. 确认所有文件已成功上传
