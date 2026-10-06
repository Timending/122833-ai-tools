# AI Agent Tools 站点说明

## 站点信息
- 域名：https://122833.xyz
- 框架：Hugo v0.139.0 extended + PaperMod主题
- 部署：GitHub Pages + GitHub Actions自动构建
- CDN：Cloudflare

## 本地操作命令

### 本地预览（边写边看效果）
```powershell
cd C:\Users\Administrator\Documents\ai-agent-tools
hugo server -D
# 打开浏览器访问 http://localhost:1313
# -D 表示包含草稿文章，正式发布时去掉-D
# Ctrl+C 停止
```

### 创建新文章
```powershell
cd C:\Users\Administrator\Documents\ai-agent-tools
hugo new content posts/my-new-article.md
# 编辑 content/posts/my-new-article.md
# 把 draft: true 改成 draft: false
# hugo server -D 预览
```

### 发布（推送到GitHub自动部署）
```powershell
cd C:\Users\Administrator\Documents\ai-agent-tools
git add .
git commit -m "Add new article"
git push
# GitHub Actions自动构建，2-3分钟后线上更新
```

## 目录结构
```
ai-agent-tools/
├── .github/workflows/hugo.yml  # GitHub Actions自动部署配置
├── content/
│   ├── about/index.md          # 关于页
│   ├── posts/                  # 博客文章
│   ├── reviews/                # 评测文章（预留）
│   └── tutorials/              # 教程文章（预留）
├── static/images/              # 图片资源
├── themes/PaperMod/            # 主题（已作为普通文件提交）
├── hugo.toml                   # 站点配置
└── README.md                   # 本文件
```

## 下一步（你需要手动做的）
1. 在GitHub创建公开仓库 ai-agent-tools
2. 推送本地代码到GitHub
3. 在GitHub仓库Settings → Pages → Source选 GitHub Actions
4. 配置Cloudflare DNS：加CNAME记录指向 YOURUSERNAME.github.io
5. 在GitHub Pages设置Custom domain为 122833.xyz
6. 等2-3分钟GitHub Actions跑完，访问 https://122833.xyz 验证

详细操作见对话中的"用户手动操作指令"部分。
