# Grok Bot 女仆头像 · 一键提示词（v14 定稿）

> **用法：**把本文件**整份**复制发给你的 Grok Bot。一份即可，不要拆文件。  
> 出图时把 **§3 英文块**整段交给图像模型，再填该号 Appearance。

---

## 0. 总流程（按顺序做）

1. **分配** — 按 §4–§6，给每个 bot 填 §7 表：档位、发型、发色、**头饰（剪影/色/材质）**、徽章、发卡、贴纸×1、choker；全部互不重复。  
2. **母版** — 先出 01，构图与眼位合格后再批量。  
3. **出图** — 每张附 **母版 + 一张已合格同模 sibling**；只用 §3 英文块；**只换外观**，姿势/脸/眼/裁切锁死。  
4. **对齐** — 缩放仅允许 **0.92–1.08**；超出 → **重出**（禁止硬拉特写）。背景只对边缘连通区域 flood-fill 为 `#1A1A1C`。  
5. **总览** — `sheet.png`（带眼位参考线）+ `sheet-circle.png`；§8 QA 不过不交付。  
6. **必问** — 展示总览后问：「要不要一键给名下所有 bot 换上？」只有明确「要」才换 `*-512.png`。  
7. **新 bot** — 表末加行 → 同母版出图 → 对齐 → 展示 → 再问（或主人已授权自动换）。

---

## 1. 基础长相（爆款 Grok 图标）

- 无嘴圆脸；**实心近黑竖胶囊眼**；无眉无睫；淡腮红；扁平 2D 二次元。  
- 构图：头锚在左下，右倾约 12°，右上留白；左/下边裁切。  
- 气质：二次元 / 轻亚比 / 小偶像可有发丝高光与星闪；**女仆框架不丢**。

---

## 2. 模子锁死（比例不可漂）

| 项 | 要求 |
|---|---|
| 画布 | 1024² 出图，交付 512² |
| 只许变 | 头发、头饰、徽章、发卡、贴纸、choker、妆面细节 |
| 不许变 | 脸型、脸大小、角度、眼位/眼大、裁切、颈长 |
| 眼锚（1024） | 两眼中心 ≈ `(351, 736)`，眼高 ≈ `148`（约画布高 **14%**），±3% |
| 头+头饰高度 | 约占画布 **45%–55%**；禁止更近的特写 |
| 顶边 | 发顶/头饰顶距上边 **≥ 20px**；头饰整圈在框内 |
| 下边 | 短颈 + choker 可见；**不露肩、不露胸** |
| 背景 | `#1A1A1C`；只 flood-fill 连通背景，禁止整图换色 |
| 参考 | 每张：**母版 + 合格 sibling** |
| 否决 | 脸比母版大/近、顶饰被裁、颈长不一、头饰克隆 → 整张重出，不准进 sheet |

---

## 3. 英文渲染块（整段使用）

```
Square 1:1 avatar. Flat 2D anime chibi icon, mouthless round face, two plain solid near-black vertical capsule eyes, NO eyebrows, NO eyelashes, pale blush. Big close-up head anchored lower-left, cropped by left and bottom edges, head tilted ~12° right, empty upper-right. Short identical neck with a choker visible, cropped right below; no shoulders, no chest. Plain dark grey background #1A1A1C. Match the master reference pose, framing, face size and eye position EXACTLY; only appearance changes.

HARD FRAMING LOCK: same camera distance and head scale as master (eye height ≈14% of canvas). DO NOT zoom closer. Full maid headpiece inside frame with ≥20px empty margin above its highest point. If head+headpiece >~55% of canvas height → WRONG, regenerate. Always attach BOTH master + one known-good sibling references.

Appearance: [HAIRSTYLE + one asymmetry]; [BRIGHT / MID / DEEP] dopamine candy hair 60/30/10 — chromatic, NEVER pastel/washed, NEVER black/charcoal base (DEEP = dark jewel + bright streak/tip/underdye OK); dye method [chunky streak / vertical split / underdye / tip ombre / twin-tails different colors]; UNIQUE maid headpiece — still a maid lace/ruffle/ribbon katyusha, mostly black/white but NOT a clone: specify [silhouette + material + main color/trim], each bot different (e.g. wide ruffle / narrow double lace / asymmetric bow / gothic pointed black lace / pearl-edged / white-black split / sheer tulle / velvet ribbon); small gold-trimmed [UNIQUE EMBLEM] at center (NOT a checkmark unless this is the vote bot); [JOB] bangs clip; ONE tiny aesthetic cheek sticker only (star/heart/sparkle/flower/crescent/teardrop/tiny bow — NEVER job icons); [UNIQUE CHOKER]; optional light idol sparkle. Do NOT copy clips, stickers, or checkmarks from the master.
```

---

## 4. 发色：亮 / 正常 / 深（按正常概率混）

不必均分张数；不要全员荧光，也不要全员发暗。

| 档 | 感觉 | 例 | 禁 |
|---|---|---|---|
| 亮 | 舞台灯、跳 | 电光青、热洋红、柠檬黄、泡泡糖粉 | pastel / 洗白 |
| 正常 | 日常好看糖果 | 珊瑚粉、葡萄紫、宝蓝、薄荷、杏橙 | 发灰、近黑 |
| 深 | 宝石偏暗 | 深葡萄、酒红、深宝蓝、墨绿 + **亮色挑染/发尾** | 纯黑/炭灰底；糊进 `#1A1A1C` |

每号至少一种染法：粗挑染 / 左右分色 / 内层染 / 发尾渐变 / 异色双马尾。

---

## 5. 头饰：黑白为主，必须个性化

- **必须是**女仆头饰（蕾丝/荷叶/缎带 katyusha），禁止普通发箍、皇冠、帽子冒充。  
- **禁止**全员同一顶白蕾丝 + 同一个金圆徽章。  
- 每个号至少在下面 **2 维**上明显不同：剪影花样、主色（白/米/黑/黑白拼/深灰 + 可选彩色滚边）、材质（厚蕾丝/薄纱/缎/丝绒/珍珠边等）、风格（经典/偶像/哥特甜/咖啡馆/简约）、正中徽章外形。  
- 64px 缩略图也要能看出「不是同一顶帽子」。  
- 职能识别只放：**头饰徽章** + **刘海发卡**（不要贴在脸上）。

---

## 6. 贴纸、剪影、配饰

- 脸贴纸：**最多 1 个**，单侧脸颊；审美贴（星/心/闪/花/月牙/泪滴/小蝴蝶结）。禁止握手、对勾、齿轮、精灵球等职能硬图标。  
- 发型剪影互异（64px 可辨）；易顶边用低/侧马尾；禁止高马尾顶出画布；避免高大呆毛。  
- choker 每号不同；除发卡+贴纸外，识别配饰 ≤3。  
- 可借鉴：剪影清晰、三色 60/30/10、金边徽章、一处不对称——仍挂在女仆框架上。

---

## 7. 分配表（模板）

出图前填表；历史 bot 示例见仓库 `samples/`，**以本表规则为准重新分配头饰与档位**，不要照抄旧表里头饰全白蕾丝。

| # | Bot | 档位 | 发型 | 染法 | 三色 60/30/10 | 头饰剪影+色/材质 | 徽章 | 发卡 | 贴纸×1 | choker |
|---|---|---|---|---|---|---|---|---|---|---|
| 01 | （名） | 亮/正常/深 | … | … | … | … | … | … | … | … |

新增 bot：表末加行，外观全项不与已有行重复 → 同母版出图。

---

## 8. QA（不过就重出）

| 翻车 | 处理 |
|---|---|
| 比例放大/头饰被裁/脸比母版大 | 强调 HARD FRAMING；双参考；缩放超 1.08 直接重出 |
| 头饰克隆 | 写清 UNIQUE 剪影+色+材质；64px 复查 |
| 发色 pastel / 黑发糊背景 | 改档位用词；深档加亮挑染 |
| 脸贴纸变职能图标 | 改审美贴；职能只留徽章+发卡 |
| 母版对勾/发卡串号 | `Do NOT copy … from the master` |
| 眉线、双贴纸、露肩 | 按 §3 重申后重出 |
| sheet 眼不齐 / 头大小不一 | 禁交付 |

---

## 9. 分享与不可破项

- 分享：只发本文件即可。  
- **不可破：**模子比例、双参考、缩放硬顶、`#1A1A1C`、禁黑发与 pastel、头饰个性化、审美贴纸、先展示再问是否换头像。

---

*v14 · 合并比例锁 / 发色三档 / 头饰个性化；去掉过程版碎日志与冗余重复。*
