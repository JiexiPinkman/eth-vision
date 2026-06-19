# CryptoVision - 加密货币与美股实时追踪平台

![CryptoVision](https://img.shields.io/badge/CryptoVision-Crypto%20%26%20Stocks-cyan?style=for-the-badge&logo=bitcoinsv)
![Status](https://img.shields.io/badge/status-Live-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

> **🚀 专业级加密货币与美股实时追踪平台 | 实时数据 | 多资产支持 | 智能预测**

---

## ✨ 支持的资产

### 🪙 加密货币
| 币种 | 名称 | 数据源 |
|------|------|--------|
| ETH | Ethereum 以太坊 | Binance / Bitfinex |
| BTC | Bitcoin 比特币 | Binance / Bitfinex |
| BNB | BNB 币安币 | Binance / Bitfinex |
| OKB | OKX 平台币 | Binance / Bitfinex |
| SOL | Solana 索拉纳 | Binance / Bitfinex |

### 📈 美股
| 股票 | 名称 | 数据源 |
|------|------|--------|
| TSLA | Tesla 特斯拉 | Yahoo Finance |
| SPXC | S&P 500 标普500 | Yahoo Finance |
| MU | Micron 美光科技 | Yahoo Finance |

---

## ✨ 核心特性

### 📊 实时价格追踪
- **多资产支持** - 一站式追踪主流加密货币和热门美股
- **毫秒级实时更新** - WebSocket 实时推送价格变动
- **多时间周期图表** - 24小时、7天、30天、90天历史数据
- **专业级 K 线图表** - 支持缩放、拖拽、数据点悬停

### 🔮 AI 智能价格预测
- **多周期价格预测** - 1小时、24小时、7天未来价格预测
- **智能置信度评估** - 基于历史波动率计算预测可信度
- **支撑阻力位分析** - 自动识别关键价格区间

### 💡 专业技术架构
- **纯前端实现** - 无需后端服务器，降低部署成本
- **响应式设计** - 完美适配桌面端、移动端、平板
- **优雅降级策略** - WebSocket 断开时自动切换轮询模式
- **现代 CSS 动画** - 流畅的交互动画体验

---

## 🎯 为什么选择 CryptoVision？

| 特性 | CryptoVision | 传统追踪器 |
|------|-------------|-----------|
| 多资产支持 | ✅ 8+ 加密货币和美股 | ❌ 仅单一资产 |
| 实时更新 | ✅ WebSocket 毫秒级 | ❌ 5-30秒轮询 |
| 价格预测 | ✅ 多周期预测 | ❌ 无 |
| 美股支持 | ✅ Yahoo Finance | ❌ 无 |
| 移动适配 | ✅ 完美响应式 | ⚠️ 勉强支持 |
| 无需注册 | ✅ 开箱即用 | ✅ 开箱即用 |
| 零成本部署 | ✅ 单文件即可 | ❌ 需要服务器 |

---

## 🛠️ 技术栈

- **前端框架**: 原生 JavaScript (ES6+)
- **图表库**: Chart.js 4.x
- **加密货币数据**: Binance API, Bitfinex API
- **美股数据**: Yahoo Finance API
- **样式**: CSS3 变量 + Flexbox + Grid + 动画
- **图标**: SVG 内联图标

---

## 🚀 快速开始

### 本地运行

```bash
# 方式一：直接打开
open index.html

# 方式二：使用 Python 简易服务器
python3 -m http.server 8080
# 然后访问 http://localhost:8080

# 方式三：使用 Node.js serve
npx serve .
# 然后访问 http://localhost:3000
```

### 部署到 GitHub Pages

1. Fork 此仓库
2. 进入 Settings → Pages
3. Source 选择 `main` branch 和 `/ (root)` 文件夹
4. 访问 `https://你的用户名.github.io/eth-vision/`

---

## 📈 界面预览

```
┌─────────────────────────────────────────────────────┐
│  ⬡ CryptoVision                                   │
│                                                     │
│  [ETH] [BTC] [BNB] [OKB] [SOL] [TSLA] [SPXC] [MU] │
│                                                     │
│  ┌─────────────────────────────────────────────┐   │
│  │  ETH Logo  Ethereum 以太坊  [加密货币]       │   │
│  │                                             │   │
│  │  $1,695.42  [实时]                         │   │
│  │  ▲ +2.35% (+$38.72)                       │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
│  [24H] [7D] [30D] [90D]                          │
│  ┌─────────────────────────────────────────────┐   │
│  │                                             │   │
│  │           📈 K线价格图表                    │   │
│  │                                             │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
│  🔮 价格预测                                       │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐         │
│  │ 1小时后   │ │ 24小时后  │ │ 7天后    │         │
│  │ $1,702   │ │ $1,745   │ │ $1,820   │         │
│  │ 置信度78% │ │ 置信度65% │ │ 置信度52% │         │
│  └──────────┘ └──────────┘ └──────────┘         │
│                                                     │
│  📊 市场统计                                       │
│  [趋势] [24h涨跌] [成交量] [高低点]              │
│                                                     │
│  🎯 关键价位                                       │
│  [支撑位] [阻力位]                                │
│                                                     │
├─────────────────────────────────────────────────────┤
│  加密货币: Binance / Bitfinex                      │
│  美股数据: Yahoo Finance                           │
│  网站制作：牛逼的严浩远                            │
└─────────────────────────────────────────────────────┘
```

---

## 📝 数据来源

| 数据类型 | 来源 | 说明 |
|---------|------|------|
| 加密货币价格 | Binance / Bitfinex | 全球主流加密货币交易所 |
| K线数据 | Binance / Bitfinex | 多交易所聚合 |
| 美股价格 | Yahoo Finance | 权威金融数据源 |

> ⚠️ 预测数据仅供参考，不构成投资建议。市场有风险，投资需谨慎。

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

## 📜 开源协议

MIT License - 自由使用、修改和分发。

---

## 👨‍💻 关于作者

**牛逼的严浩远** - 全栈开发者，专注于 Web3 和金融科技领域

- 🔗 GitHub: [@yanhaoyuan](https://github.com/yanhaoyuan)
- 💼 LinkedIn: [Yanhaoyuan](https://linkedin.com/in/yanhaoyuan)

---

<p align="center">
  <strong>Made with ❤️ by <a href="https://github.com/yanhaoyuan">牛逼的严浩远</a></strong>
  <br>
  <sub>让加密货币和美股追踪变得简单而优雅</sub>
</p>
