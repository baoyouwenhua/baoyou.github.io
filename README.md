```markdown
# 🎮 包游战场

> 手机可玩的联机射击游戏 · 打开浏览器即玩

👉 **[点这里在线试玩](https://baoyouwenhua.github.io/baoyou.github.io/)** ｜ [MIT 协议](./LICENSE)

---

## 📖 简介

基于浏览器 2D 俯视角联机射击游戏。游客免注册即可玩，正式账号可保存战绩。

## ✨ 特性

**玩法**
- 单人模式：10 人混战，AI 补齐
- 团队模式：1v1 ~ 5v5，10 分钟一局
- 武器：手枪 / 步枪 / 狙击 / 机枪 / 长刀
- 金币：站灰块挂机赚钱，去商人处买枪
- 道具：血包 / 超血 / 能量饮料

**AI**
- 随机武器，会刷钱、会买枪、会残血逃跑
- 不同武器不同打法：长刀贴脸、狙击拉远、机枪中距

**社交**
- 登录注册、好友、私信
- 世界聊天（单/团队独立频道，消息 10 秒消失）
- 举报 + 管理员后台（封禁 / 审核）

**战绩**
- 金币 / 击杀 / 死亡跨局保存
- 首页击杀榜 Top 20

**音效投票**
- 8 种 Web Audio 实时合成音效，玩家试听 + 投票

## 🕹️ 操作

**电脑**：WASD 移动 · 鼠标瞄准 · 左键开火 · Q 换枪 · R 换弹 · F 商店 · 1/2/3 用药 · ESC 退出  
**手机**：左下摇杆移动 · 点击屏幕瞄准 · 右下按钮开火/换弹/换枪 · 摇杆上方用药

## 🛠️ 技术栈

- 前端：HTML + CSS + 原生 JS + Canvas 2D（无框架、无打包）
- 后端：Supabase（数据库 + Realtime）
- 部署：GitHub Pages
- 音效：Web Audio API 实时合成

## 📁 结构

```

├── index.html     # 大厅（登录/好友/私信/排行榜/后台）
├── solo.html      # 单人模式
├── team.html      # 团队模式
├── vote.html      # 音效投票
├── README.md
└── LICENSE

```

## 🗄️ 主要数据库表

| 表 | 用途 |
|---|---|
| `battle_users` | 账号（金币/击杀/死亡/封禁） |
| `battle_social` | 好友 + 私信 |
| `battle_world_chat` | 团队世界聊天 |
| `battle_world_chat_solo` | 单人世界聊天 |
| `battle_chat_reports` | 聊天举报 |
| `battle_sfx_votes` | 音效投票 |

## 🚀 本地跑

1. 注册 [Supabase](https://supabase.com) 拿 URL + KEY
2. 建表 + 建 RPC 函数
3. 改代码里两行：

```js
var SUPABASE_URL = "你的 URL";
var SUPABASE_KEY = "你的 KEY";
```

4. 起本地服务：python -m http.server 8080

❓ 常见问题

· 游客看不到战绩？ 游客是临时的，注册正式账号才保存
· 单人/团队聊天互通吗？ 不互通，独立频道
· 聊天记录消失？ 设计如此，10 秒自动清理
· 加好友搜不到？ 对方得是正式账号，游客搜不到

📝 更新日志

· v0.3.0 — 双模式、AI 智能、世界聊天、战绩保存、排行榜、音效投票
· v0.2.0 — 登录注册、好友私信、举报审核
· v0.1.0 — 项目起步

🙏 致谢

后端 Supabase · 部署 GitHub Pages

📄 协议

MIT License — 可自由使用、修改、商用，保留署名即可。

📮 联系

· B 站：翻译中请投币小号
· QQ 邮箱：hk_3@qq.com
· GitHub：@baoyouwenhua
· 反馈：Issues

---

<p align="center"><strong>🎮 玩得开心！</strong><br><sub>Made with ❤️ by 包游文化</sub></p>
```
