# CHUNIDATA

非官方 CHUNITHM 国服成绩助手 Web MVP，部署到 GitHub Pages。

## 功能（v0.2.0）
- 水鱼公开 CHUNITHM 曲库 `GET /music_data`，歌曲/谱面定数及难度检索
- 获取 `GET /latest_version` 并显示新曲版本
- 公开可查询用户名的 `POST /query/player`，展示 Rating 和 B30/N20
- `GET /player/test_data` 用于无账户的官方 API 测试数据
- 实验性推分建议：按已入榜 RA 由低到高列出可复查谱面，**不是精确推分预测**
- 本地设置、缓存、刷新、检查发布版本
- GitHub Actions 自动部署静态网站

## 部署
Settings → Pages → Source 选择 GitHub Actions，推送 `main` 自动运行 `.github/workflows/deploy.yml`。预期网址：https://observl.github.io/chunidata/

## 数据权限及限制
- **静态网站不支持安全的私有 OAuth 和二维码登录。** 不要在页面粘贴扫码登录凭证、密码、Bearer/Import Token。
- 浏览器跨域可能被 Diving-Fish API 的 CORS 策略阻止；生产环境需要经批准的后端同源代理，不应绕过数据源访问政策。
- 公开用户名的成绩查询受水鱼用户隐私设置约束；若拒绝查询请在水鱼使用正规授权机制。
- 本网页不从国服官方服务器自动抓取最新数据；水鱼最新数据依赖其自行同步。
- 无微信小程序及微信封面广告支持。
- 游戏商标及曲库数据归各自权利人所有。商用须确认接口和资产使用许可。

参考：[Diving-Fish API 文档](https://maimai.diving-fish.com/manual/docs/developer/zh-api-document/) · [OAuth 文档](https://maimai.diving-fish.com/manual/docs/developer/oauth-api-document/)
