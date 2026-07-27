# Shuzhi Xu — Academic Website

这是个人学术主页的 Jekyll 源代码，基于 AcademicPages 主题。

## 主要内容

- `_pages/about.md`：首页
- `_pages/research.md`：研究方向
- `_pages/publications.md`：论文列表
- `_pages/Software.md`：软件
- `_pages/cv.md`：简历
- `_portfolio/`：研究详情页
- `project/BsplineTO/`：独立的交互式项目页面
- `images/`：网站实际使用的图片

## 本地预览

```bash
bundle install
bundle exec jekyll serve
```

浏览器打开 `http://localhost:4000`。

## 发布

将代码推送到 GitHub Pages 仓库即可触发自动构建。不要把 `_site/`、`.sass-cache/`、`node_modules/` 或本地 `.git/` 历史打进分发压缩包。

主题许可见 `LICENSE`。

bundle exec jekyll serve
git add .
git commit -m "Update homepage"
git push origin main


