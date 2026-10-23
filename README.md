# Grok Bot 女仆头像 · 一键提示词

一套给 Grok Bot 用的女仆头像提示词：全员同一张脸、同一个构图，头发和头饰各不一样；发色亮/正常/深混着来；**深色头饰绝不糊进 `#1A1A1C`**。把提示词整份丢给你的 Bot，它会先出总览，再问你要不要一键换上。

## 效果预览

24 张同模 showcase（v16：深色头饰已加亮滚边 / 外白荷叶 / 浅主色；6×4）：

![6x4 showcase](samples/sheet-6x4.png)

单张示例：

| 亮·电光青 | 正常·薄荷珍珠 | 深·酒红 | 正常·珊瑚 | 深·翠绿 | 亮·粉青分色 |
|:---:|:---:|:---:|:---:|:---:|:---:|
| ![s01](samples/s01-bright-cyan.png) | ![s06](samples/s06-deep-grape.png) | ![s12](samples/s12-deep-wine.png) | ![s19](samples/s19-mid-coral.png) | ![s20](samples/s20-deep-emerald.png) | ![s21](samples/s21-bright-split.png) |

## 怎么用

1. 打开本仓库里的 [`PROMPT.md`](PROMPT.md)（或直接展开下面的「完整提示词」），**整份复制**。
2. 粘贴发给你的 **Grok Bot**（或 Cursor 助手）。
3. Bot 会按同一个模子出一套图，并先给你看总览图。
4. 看完后它会问一句：**「要不要一键给你名下所有 bot 都换上这套头像？」**
5. 你说「要 / 换上」它才换；说「先不换」就只留图。

> 不要拆成两个文件用——一份提示词就够。

## 效果约定

- **同一个模子**：脸型、眼睛位置、歪头角度、裁切一致；只换头发、头饰、徽章、发卡、贴纸、choker。
- **构图**：大特写锚在左下，露一小截脖子 + choker，不露肩膀和胸口；背景 `#1A1A1C`。
- **发色**：饱和多巴胺糖果色，**亮 / 正常 / 深**按自然比例混搭（深档用宝石底+亮挑染）；保留挑染 / 分色 / 内层染 / 发尾渐变；**不要黑发，也不要水洗浅色**。
- **头饰**：必须是女仆蕾丝/荷叶/缎带 katyusha；**黑白为主**但剪影、材质、滚边、徽章外形要互异（禁止全员同一顶白蕾丝）。
- **深色头饰对比锁（v16）**：黑/炭灰头饰在 `#1A1A1C` 上必须可读——亮滚边（象牙/奶油/银/金/高饱和色 ≥2px）/ 换浅主色（奶油/米/浅灰/酒红）/ 外白内黑荷叶边，三选一；禁止哑光纯黑无边。
- **贴纸**：每边脸最多 1 个审美贴（星星、爱心、月牙等），不放握手、对勾这类硬图标；职能识别只在头饰徽章和发卡上。
- **气质**：二次元 / 轻亚比 / 一点点小偶像，女仆框架不丢。

## 完整提示词（v16）

<details>
<summary>点击展开：一键提示词 v16（复制这里或 PROMPT.md）</summary>

# Grok Bot 女仆头像 · 一键提示词（v16）

> **给你用的：**整份复制 → 发给你的 Grok Bot。  
> **给 Bot 用的：**先看「做成什么样」，再严格按流程；出图时把 **§3 英文**整段交给画图模型。

---

## 做成什么样（验收标准）

一套图摊开看，应该是：

1. **同一张脸、同一个镜头** — 眼睛齐平、头一样大，像换装不是换人。  
2. **发色有层次** — 亮 / 正常 / 深都有，不是全员荧光，也不是全员发暗；没有黑发、没有水洗浅粉。  
3. **头饰一眼能分清** — 仍是女仆头饰，但以黑白为主，花样、材质、风格各不相同（不是复制同一顶白蕾丝）。  
4. **深色头饰绝不糊进背景** — 黑/炭灰头饰在 `#1A1A1C` 上必须能看清轮廓（亮滚边 / 换浅主色 / 外层白荷叶边三选一）；缩略图也能看出头饰剪影。  
5. **配饰有记忆点** — 发卡、颈链、脸颊小贴纸每号不一样；贴纸是可爱装饰，不是工作图标。  
6. **先给总览，再问要不要换** — 没问就换 = 做错了。

做不到以上任一条：重做，不要凑合交付。

---

## 0. 流程（按顺序）

1. 按 §4–§6 给每个助手填 §7 表（外观全不重复）。  
2. 先出 **01 母版**，构图合格再批量。  
3. 每张出图附上：**母版图 + 一张已经合格的同套图**；只用 §3 英文；只改外观。  
4. 对齐：整体缩放只能在 **0.92～1.08**；超出就重画，不要靠放大硬修。背景只把「连到画布边缘的底色」填成 `#1A1A1C`（不要整张图一起染色，免得头发被染脏）。  
5. 出总览图（眼睛一条线）→ 用 §8 自检 → 给用户看。  
6. 问：「要不要一键给名下所有 bot 换上这套头像？」只有明确说要才换。  
7. 以后新助手：表里加一行 → 同母版出图 → 再问（或主人已说过可以自动换）。

---

## 1. 基础长相

- 圆脸、**没有嘴巴**；两只**实心近黑竖胶囊眼睛**；没有眉毛、没有睫毛；一点点腮红。  
- 扁平二次元小头像；头靠左下，稍微向右歪，右上留空；左边和底边被裁掉一点。  
- 可以有发丝高光、小星星闪光；但必须还是女仆系，不要变成普通美少女头像。

---

## 2. 模子锁（比例不能漂）

| 项 | 要求 |
|---|---|
| 画布 | 先画 1024×1024，交付再缩 512×512 |
| 可变 | 头发、头饰、徽章、发卡、贴纸、颈链、小妆点 |
| 不可变 | 脸型、脸大小、角度、眼睛位置和大小、裁切、脖子长短 |
| 眼睛（1024 图） | 两眼中心大约 `(351, 736)`，眼高大约 `148`（约画面高度的 **14%**），误差 ±3% |
| 头+头饰 | 约占画面高度 **45%～55%**；不许拍得更近 |
| 上边 | 头饰最高点距顶 **≥ 20px**，头饰完整不进裁 |
| 下边 | 露出一小截一样长的脖子和颈链；不露肩膀、不露胸口 |
| 背景 | `#1A1A1C` |
| 参考 | 每张都要：**母版 + 一张合格同套图** |
| 直接作废 | 脸变大/变近、头饰被切、脖子长短不一、头饰复制粘贴、深色头饰糊进背景 |

---

## 3. 英文出图块（整段复制给画图模型）

先锁构图，再写外观。Appearance 里把方括号换成这一号的具体词；不要留空括号。

```
Square 1:1 avatar. Flat 2D anime chibi icon, mouthless round face, two plain solid near-black vertical capsule eyes, NO eyebrows, NO eyelashes, pale blush. Big close-up head anchored lower-left, cropped by left and bottom edges, head tilted ~12° right, empty upper-right. Short identical neck with a choker visible, cropped right below; no shoulders, no chest. Plain dark grey background #1A1A1C.

FRAMING LOCK (match master exactly): same pose, same face size, same eye position, same camera distance. Eye height ≈14% of canvas. Head + maid headpiece ≈45–55% of canvas height — DO NOT zoom closer. Entire headpiece inside frame with ≥20px empty margin above it. Attach BOTH the master image AND one known-good sibling from this set as references. If framing drifts, regenerate; do not crop tighter.

Appearance: [concrete hairstyle + one asymmetry]. [BRIGHT or MID or DEEP] dopamine candy hair in 60/30/10 colors [name three colors] — rich chromatic candy, NEVER pastel/washed pink, NEVER black/charcoal base (if DEEP: dark jewel base + bright streak or tip). Dye: [chunky streak / vertical split / underdye / tip ombre / different-color twin tails]. UNIQUE maid headpiece (must still read as maid lace/ruffle/ribbon band; mostly black/white; NOT a clone of other bots): [silhouette], [material], [main color + REQUIRED contrast treatment if dark — see HEADPIECE CONTRAST LOCK], center gold-trimmed emblem shaped like [unique symbol — not a checkmark unless vote bot]. Bangs clip: [job prop]. ONE tiny aesthetic cheek sticker only: [star/heart/sparkle/flower/crescent/teardrop/tiny bow] — NEVER job icons. Choker: [unique]. Optional soft hair sparkle. Do NOT copy any clip, sticker, or checkmark from the master.

HEADPIECE CONTRAST LOCK (non-negotiable on #1A1A1C): Dark / black / charcoal / near-black headpieces MUST stay readable at thumbnail size. For ANY dark headpiece pick ONE: (a) bright edge piping ≥2px visual — ivory, cream, silver, gold, or hot color along the ENTIRE outer silhouette; OR (b) swap the main body to cream / ivory / soft grey / wine with contrast lace; OR (c) white/cream outer frill wrapping a dark inner band. NEVER pure matte black lace with no rim. Far-thumbnail must show the headpiece silhouette clearly against #1A1A1C.
```

**合格 Appearance 示例 A（投票号 · 白头饰，可仿写）：**

```
Appearance: long straight hair with blunt bangs, one longer strand on the left. MID dopamine candy hair 60/30/10 hot coral / cream / lemon gold — tip ombre. UNIQUE maid headpiece: wide white layered ruffle lace, thick lace material, ivory white with thin gold piping, center gold-trimmed emblem shaped like a ballot check. Bangs clip: tiny paper ballot. ONE tiny aesthetic cheek sticker only: gold teardrop sparkle. Choker: thin gold-edged white lace with a small gold ring. Soft hair sparkle. Do NOT copy any clip, sticker, or checkmark from the master.
```

**合格 Appearance 示例 B（深色头饰 · 必须有亮滚边，可仿写）：**

```
Appearance: low side braid with soft bangs, one longer left strand. DEEP dopamine candy hair 60/30/10 deep grape jewel / neon lilac streak / lemon gold — underdye. UNIQUE maid headpiece: gothic pointed scallop lace, thick lace material, charcoal black INNER band wrapped by a bright ivory outer frill PLUS thin hot-pink piping ≥2px on the entire outer silhouette (HEADPIECE CONTRAST LOCK — never matte black alone), center silver-trimmed emblem shaped like a cherry blossom. Bangs clip: tiny grape flower. ONE tiny aesthetic cheek sticker only: cream star. Choker: velvet purple with a silver bell. Soft hair sparkle. Do NOT copy any clip, sticker, or checkmark from the master.
```

---

## 4. 发色：亮 / 正常 / 深

按平常感觉混，不必平均张数。

| 档 | 感觉 | 可以 | 不要 |
|---|---|---|---|
| 亮 | 舞台灯 | 电光青、热洋红、柠檬黄、泡泡糖粉 | 水洗浅粉 |
| 正常 | 日常好看 | 珊瑚粉、葡萄紫、宝蓝、薄荷、杏橙 | 发灰、发脏 |
| 深 | 宝石偏暗 | 深葡萄、酒红、深宝蓝、墨绿，并加亮色挑染或发尾 | 纯黑、炭灰；暗到跟背景糊在一起 |

---

## 5. 头饰：黑白为主，必须能分清 + 深色可读

- 必须是女仆头饰（蕾丝、荷叶边、缎带发箍那种），不要改成普通发箍、皇冠、帽子。  
- 禁止全员同一顶白蕾丝、同一个圆形金徽章。  
- 每个号至少在两项上明显不同：外形花样、颜色（白/米/黑/黑白拼/深灰，可加彩色滚边）、材质、风格、正中徽章形状。  
- **深色 / 黑色 / 炭灰头饰硬规则（不可妥协）：**在 `#1A1A1C` 背景上必须可读。任选其一——  
  1. **亮滚边**：整圈外轮廓象牙/奶油/银/金/高饱和色描边，视觉宽度 ≥2px；或  
  2. **换主色**：主体改成奶油/象牙白/浅灰/酒红，再配对比色蕾丝；或  
  3. **外白内黑**：白色/奶油色外层荷叶边包住深色内带。  
  **禁止**纯哑光黑蕾丝、无任何滚边/外白边。远看缩略图必须能看出头饰剪影。  
- 缩成很小也能看出来「不是同一顶」。  
- 谁是哪个职能：只靠 **头饰徽章** 和 **刘海发卡**，不要画在脸上。

---

## 6. 贴纸、发型、颈链

- 脸颊贴纸最多 1 个，只贴一边；星星、爱心、闪光、小花、月牙、泪滴、迷你蝴蝶结。不要握手、对勾、齿轮、精灵球。  
- 发型外形各不相同；容易顶到上边的用低马尾或侧马尾；不要高马尾顶出画面；少用又高又大的呆毛。  
- 颈链每号不同；除发卡和贴纸外，额外识别小件不超过 3 个。  
- 追求：缩略图能认出谁是谁；颜色 60/30/10；金色小点缀；全身只做一处明显不对称。

---

## 7. 分配表

出图前填满。头饰列一定要写清「外形 + 材质 + 颜色 + 对比处理（若深色）」，不要只写「白蕾丝」或「黑蕾丝」。

| # | 助手名 | 档位 | 发型 | 染法 | 三色 | 头饰（外形/材质/色/对比） | 徽章 | 发卡 | 贴纸 | 颈链 |
|---|---|---|---|---|---|---|---|---|---|---|
| 01 | （例）投票 | 正常 | 齐刘海长直 | 发尾渐变 | 热珊瑚/奶油/柠檬金 | 宽层叠白蕾丝/厚蕾丝/米白描金 | 选票对勾 | 小选票 | 金泪滴 | 金边白蕾丝+金环 |
| 02 | （例）深色头饰 | 深 | 侧辫软刘海 | 内层染 | 深葡萄/霓虹紫/金 | 哥特尖扇蕾丝/厚蕾丝/炭灰内带+象牙白外荷叶+热粉滚边 | 樱花 | 葡萄花 | 奶油星 | 紫绒+银铃 |
| 03 | … | … | … | … | … | … | … | … | … | … |

新助手：表末加行，外观不与已有重复 → 同一母版出图。

---

## 8. 自检（不过就重画）

| 问题 | 怎么办 |
|---|---|
| 越到后面脸越大、头饰被切 | 检查英文 FRAMING LOCK；双参考；缩放超过 1.08 直接重画 |
| 头饰长一个样 | 分配表重写外形/材质/色；缩略图复查 |
| 头发太浅或发黑糊进背景 | 换档位用词；深档加亮挑染 |
| **深色头饰糊进 #1A1A1C** | 加亮滚边 / 换浅主色 / 外白荷叶边；禁止哑光纯黑无边 |
| 脸上出现工作图标 | 改成可爱小贴；职能只留徽章和发卡 |
| 母版的对勾跑到别的号 | 英文写清不要抄母版配件 |
| 总览眼睛不齐、头大小不一 | 不准交付 |

---

## 9. 分享时请保留

- 只需分享本文件（或本仓库）。  
- **不要删：**同一模子、双参考、缩放上限、背景色、禁黑发与水洗浅色、头饰要能分清、**深色头饰对比锁**、可爱贴纸、先展示再问是否更换。

---

*v16 · 在 v15 验收标准与展示友好基础上，新增深色头饰对比硬锁（亮滚边 / 换浅主色 / 外白内黑），禁止哑光黑蕾丝糊进 #1A1A1C。*


</details>

## 版本

- **v16** — 深色头饰对比硬锁；showcase 重画过暗槽位（s04/s05/s08/s11/s15/s22）。
- v15 — 验收标准前置、英文分锁构图/写外观、合格 Appearance 示例、中文口语化。
- 更早版本见 git 历史。

## License

提示词与示例图可自由用于个人 Grok Bot / Cursor 助手头像；转载请保留本仓库链接与「先展示再问是否更换」约定。
