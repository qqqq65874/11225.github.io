# Cloudflare Pages 部署说明

本项目是一个静态个人简介网页，包含 `index.html`、`avatar.jpg` 和 `wechat-qrcode.jpg`。

## 网站结构

- `index.html` — 网站首页
- `avatar.jpg` — 头像图片
- `wechat-qrcode.jpg` — 微信二维码图片

## 部署步骤

1. 创建 Git 仓库
   ```bash
   cd "c:\Users\Administrator\Desktop\my web"
   git init
   git add .
   git commit -m "初始提交"
   ```

2. 推送到 GitHub
   - 在 GitHub 上创建一个新仓库
   - 将本地仓库与 GitHub 仓库关联并推送
   ```bash
   git remote add origin <your-github-repo-url>
   git branch -M main
   git push -u origin main
   ```

3. 在 Cloudflare Pages 上配置
   - 登录 Cloudflare 仪表盘
   - 进入 Pages，选择“创建项目”
   - 连接到你的 GitHub 仓库
   - 部署设置：
     - Branch：`main`（或你使用的分支）
     - Framework preset：`None` / 无
     - Build command：留空
     - Build output directory：留空或填 `.`

4. 发布
   - 点击“保存并部署”
   - 部署完成后，访问 Cloudflare Pages 提供的站点 URL

## 注意事项

- 图片使用相对路径引用，确保 `avatar.jpg` 和 `wechat-qrcode.jpg` 都在站点根目录。
- 如果你想更改姓名、内容或图片，只需编辑 `index.html` 并重新提交到 GitHub。
