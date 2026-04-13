# 禅语日历 - GitHub Pages

这是禅语日历应用的官方网站，包含以下页面：

- `index.html` - 营销主页（App 介绍和下载）
- `support.html` - 技术支持页面
- `privacy.html` - 隐私政策页面

## 部署到 GitHub Pages

### 方法 1: 通过仓库设置部署

1. 将 `docs` 文件夹推送到 GitHub 仓库
2. 进入仓库的 Settings -> Pages
3. Source 选择 "Deploy from a branch"
4. Branch 选择 `main` 分支，文件夹选择 `/docs`
5. 点击 Save

几分钟后，您的网站将部署到：
```
https://[your-username].github.io/[repository-name]/
```

### 方法 2: 使用 GitHub Actions

项目已包含 `.github/workflows/pages.yml` 配置文件，推送代码后会自动部署。

## 更新 App Store 链接

部署成功后，请在以下文件中更新实际的 App Store 下载链接：

1. `index.html` - 将 `<a href="#" class="download-btn">` 中的 `#` 替换为您的 App Store 链接
2. 搜索所有 `href="#"` 并替换为实际链接

## 更新联系邮箱

在以下文件中替换示例邮箱为您的真实邮箱：

- `support.html`
  - `support@example.com` → 您的技术支持邮箱
  - `feedback@example.com` → 您的用户反馈邮箱
- `privacy.html`
  - `privacy@example.com` → 您的隐私咨询邮箱

## 填写 App Store 元数据

部署完成后，在 App Store Connect 中填写以下 URL：

- **技术支持 URL**: `https://[your-username].github.io/[repository-name]/support.html`
- **营销网址 URL**: `https://[your-username].github.io/[repository-name]/`
- **隐私政策网址 URL**: `https://[your-username].github.io/[repository-name]/privacy.html`

## 自定义域名（可选）

如果您有自定义域名：

1. 编辑 `CNAME` 文件，填写您的域名（如 `calendar.yourdomain.com`）
2. 在您的域名注册商处添加 DNS 记录：
   - 类型: CNAME
   - 名称: calendar（或您选择的子域名）
   - 值: [your-username].github.io

## 本地预览

在 `docs` 文件夹中运行：

```bash
python3 -m http.server 8000
```

然后访问 `http://localhost:8000`

## 许可

© 2026 禅语日历. All rights reserved.
