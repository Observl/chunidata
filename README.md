# CHUNIDATA
非官方 CHUNITHM 成绩助手——可通过 GitHub Pages 部署的可用静态 MVP。

## 网站
启用仓库 GitHub Pages 的 **Source: GitHub Actions** 后，预期地址为：https://observl.github.io/chunidata/

## 当前支持
- 响应式成绩总览（Rating/B30/N20 仅为显著标注的虚构演示值）
- 手动录入歌曲成绩、按名称搜索、按难度筛选
- 浏览器 localStorage 本地保存和删除成绩，无需后端
- 推送到 main 触发 .github/workflows/deploy.yml 自动发布

## 尚未支持
- 国服二维码身份绑定、真实成绩拉取、Diving-Fish OAuth、Rating 精确计算
- 微信小程序、微信封面广告（GitHub Pages 网站不是微信小程序）

**不要向本站输入国服登录二维码文本、Token 或账号密码。** 真正的成绩同步需要明确数据源许可，并增加安全后端。

## 发布
1. 打开仓库 Settings → Pages。
2. 在 **Build and deployment → Source** 选择 **GitHub Actions**。
3. 打开 Actions，运行 “Deploy CHUNIDATA to GitHub Pages” 或推送到 main。
4. 在 Actions 确认工作流成功，再访问上述 URL。

## 本地使用
直接打开 index.html；不需要 Node、npm 或构建步骤。
