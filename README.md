# 🚢 挪亞方舟・動物上船(hfpc-noahark-match3)

「Candy Crush 骨架 + tsum 可愛外皮」系列首發:**swap 三消反向化**(match3-swap 範式)
+ **tsum 圓萌臉**(圓滾滾+豆豆眼+腮紅)+ **squash & stretch Q 彈動畫**(可愛靠動畫,不靠物理)。

- 骨架:`hfpc-paul-game/src/minigames/manna/game.js`(嗎哪收取,系列類型⑰)
- 皮:tsum 家族(fiveloaves 等八款)圓臉畫法
- 經文:創 6:19-20、7:9、7:16、8:7、9:13——**均經 cuv MCP 逐字查證(和合本)**

## ⚠ 審核狀態

**文案待牧者審核,過審前不進大廳卡。**
另:同題材已有 `arkmatch`(彈珠配對・各從其類,創 7,已過審)——本關信息刻意區隔:
**「一對一對上船」(創 7:9)+「虹=立約記號」(創 9:13)**;兩關並存與否請牧者定奪。

## 玩法(消消樂反向化,永不會輸)

- 點兩隻相鄰動物交換;排成 3 隻同款=「一起上船」(飛進方舟,艙房窗一格格亮)——**收納,不是消滅**
- 補位=動物從遠方走來(創 6:20「要到你那裡」:動物是神招聚來的)
- 連 4+ 出**彩虹方塊**:點一下整排整列一起上船(恩典多給,同 glean 語意)
- **烏鴉**(創 8:7,童/青檔):飛來擋路、不能配對,過一會自己飛走;不扣分
- 無步數/時間限制;換不成=溫柔換回;無手可動=溫柔重洗,進度保留
- 年齡三檔:幼 6×6・20 對/童 7×7・32 對(烏鴉2)/青 8×8・45 對(烏鴉3)

## 開發

零相依、零美術檔、可離線(PWA)。本機直開 `index.html` 或任一靜態 server。
語音重烤:`node scripts/gen-tts.mjs`(曉臻;相依走隔壁 hfpc-paul-game 的 node_modules)。
測試掛勾:`window.__m3.start('kid')` / `window.__m3.state()`。

## 部署(CF Workers assets,手動)

```bash
npx wrangler deploy --name hfpc-noahark-match3 --compatibility-date 2026-07-01 --assets .
```

改版時 `sw.js` 的 `CACHE_NAME` 版本 +1。`.assetsignore` 已擋 `.git`/`.wrangler`(daniel 07-23 教訓)。
