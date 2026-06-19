# ETHVision - Ethereum Price Display & Prediction

## 1. Project Overview

- **Project Name**: ETHVision
- **Project Type**: Single-page cryptocurrency dashboard
- **Core Functionality**: Real-time ETH price display with AI-powered price predictions
- **Design Philosophy**: Minimalist, clean, futuristic with sci-fi aesthetics
- **Target Users**: Crypto enthusiasts who want a clean, at-a-glance ETH price tracker

## 2. Visual Design

### Color Palette
- **Background**: Deep dark (#0a0a0f) with subtle grid pattern
- **Primary Accent**: Cyan (#00f0ff) - electric blue for highlights
- **Secondary**: Purple (#a855f7) - for gradients and accents
- **Success**: Emerald (#10b981) - bullish/positive indicators
- **Danger**: Rose (#f43f5e) - bearish/negative indicators
- **Text Primary**: White (#ffffff)
- **Text Secondary**: Slate (#94a3b8)
- **Glass Effect**: rgba(255,255,255,0.05) with backdrop-blur

### Typography
- **Font Family**: Inter (Google Fonts) - clean, modern sans-serif
- **Price Display**: 72px bold, monospace feel
- **Headings**: 24px semibold
- **Body**: 14px regular
- **Numbers**: Tabular numerals for alignment

### Layout Structure
```
┌─────────────────────────────────────────┐
│  ETHVision                    [Theme]   │  Header
├─────────────────────────────────────────┤
│                                         │
│         ◉ ETH PRICE: $3,456.78          │  Hero Price
│         ▲ +2.34% (24h)                  │
│                                         │
├─────────────────────────────────────────┤
│  ┌─────────┐ ┌─────────┐ ┌─────────┐   │
│  │ 1H Pred │ │ 24H Pred│ │ 7D Pred │   │  Predictions
│  │ $3,489  │ │ $3,512  │ │ $3,678  │   │
│  │  ↑ 0.9% │ │  ↑ 1.6% │ │  ↑ 6.4% │   │
│  └─────────┘ └─────────┘ └─────────┘   │
├─────────────────────────────────────────┤
│  [24H] [7D] [30D] [90D]                 │
│  ╭─────────────────────────────────╮    │
│  │                                 │    │
│  │        Price Chart Area         │    │  Chart
│  │                                 │    │
│  ╰─────────────────────────────────╯    │
├─────────────────────────────────────────┤
│  Market Cap    24h Volume    Dominance  │
│  $415.2B       $18.5B        17.2%      │  Stats
├─────────────────────────────────────────┤
│  Support: $3,234  │  Resistance: $3,678 │  Levels
└─────────────────────────────────────────┘
```

### Visual Effects
- Subtle animated grid background
- Glowing border effects on cards
- Smooth number transitions
- Pulse animation on live price
- Gradient text effects
- Glass morphism cards with blur

## 3. Data & Prediction Logic

### Data Source
- **Primary**: CryptoCompare API (CORS enabled) - 免费好用，支持实时价格
  - REST Ticker: `https://min-api.cryptocompare.com/data/pricemultifull?fsyms=ETH&tsyms=USD`
  - Historical: `https://min-api.cryptocompare.com/data/v2/histominute|histohour|histoday`
  - WebSocket: `wss://streamer.cryptocompare.com/v2` (订阅 CCCAGG~ETH~USD 频道)
- **轮询策略**: 每秒通过 REST API 获取实时数据
- **图表**: 显示历史K线 + 实时价格点(最近60个点)

### Prediction Algorithm
Simple momentum-based prediction:
- **1H Prediction**: Current price × (1 + hourly_momentum)
- **24H Prediction**: Current price × (1 + daily_momentum × 0.8 + volume_factor × 0.2)
- **7D Prediction**: Current price × (1 + weekly_momentum × 0.6 + sma_trend × 0.4)

### Momentum Calculation
```
momentum = (current_price - past_price) / past_price
volume_factor = current_volume / avg_volume
confidence = 1 / (1 + volatility)
```

## 4. Interaction Specification

### Controls
- Timeframe selector buttons (24H, 7D, 30D, 90D)
- Auto-refresh toggle (updates every 60s)
- Theme toggle (dark/light) - default dark

### Animations
- Price counter animation on load
- Gentle pulse on current price
- Smooth card hover effects
- Chart line animation on data load

## 5. Technical Implementation

### Stack
- Single HTML file with embedded CSS and JavaScript
- No build tools required
- Chart.js for price visualization
- Native fetch API for data

### File Structure
```
eth-vision/
  index.html    # Complete single-page app
  SPEC.md       # This specification
```

## 6. Acceptance Criteria

1. ✅ Clean, minimalist interface with futuristic feel
2. ✅ Display current ETH price prominently
3. ✅ Show 3 prediction timeframes (1H, 24H, 7D)
4. ✅ Interactive price chart with timeframe selection
5. ✅ Display key market stats
6. ✅ Support/resistance levels
7. ✅ Auto-refresh functionality
8. ✅ Smooth animations and transitions
9. ✅ Responsive design for all screen sizes
10. ✅ Works without API (fallback to demo data)
