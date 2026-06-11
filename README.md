# Wellcee 个人资料完善流程改版 · 交互原型

一个自包含的手机端交互原型,演示把 AI 溶进资料完善表单的三屏流程(编辑基础 → 标签兴趣 → 资料预览)。
纯静态:无后端、不调用任何 AI API,所有"AI 生成"的简介都是预写内容,通过前端切换。

## 本地预览
直接用浏览器打开 `index.html` 即可,无需服务器。

## 部署到 Railway

方式一 · 从 GitHub 部署(推荐)
1. 把 `index.html` 和 `package.json` 推到一个 GitHub 仓库。
2. Railway → New Project → Deploy from GitHub repo,选这个仓库。
3. Railway 会自动识别为 Node 项目,执行 `npm install` 后运行 `npm start`(用 `serve` 托管,自动读取 Railway 注入的 `$PORT`)。
4. Settings → Networking → Generate Domain,拿到公开访问链接。

方式二 · Railway CLI
1. 安装 CLI:`npm i -g @railway/cli`,然后 `railway login`。
2. 在本目录执行 `railway init`,再 `railway up`。
3. 同样在 Settings 里生成域名。

## 交互说明
- 屏 1/2:点「下一步」前进,点左上「‹」返回。
- 屏 3:语言 tab(EN / 中文 / NL)、语气切换(真诚 / 俏皮 / 简洁)、「换个说法」、加细节 chip(点开填一个短词,自动缝进简介并高亮)、简介可就地编辑。
