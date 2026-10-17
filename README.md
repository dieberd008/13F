# 13F 增仓雷达

公开静态演示页： [打开网站](https://dieberd008.github.io/13F/)

页面使用随 HTML 发布的 SEC 报告快照，可直接浏览，无需本地安装。快照有时滞，不是实时行情或投资建议。

## 实时查询

实时查询功能需要服务端代理 SEC 请求并配置 `SEC_USER_AGENT`。GitHub Pages 只托管静态文件，不能运行本项目的 Node.js 服务端；因此此 Pages 地址展示快照，不提供实时查询。需要实时查询请在本地使用 Node.js：

```powershell
Copy-Item .env.example .env
# 在 .env 中设置 SEC_USER_AGENT 为带真实联系邮箱的标识
npm start
``

然后访问 http://localhost:3000。不要将含有真实邮箱、令牌或密钥的 `.env` 上传到公开仓库。

数据来自 SEC EDGAR 13F-HR。13F 是季度末持仓披露，通常有延迟，仅代表报告时点持仓，不代表实时交易或投资建议。
