# THE DIGITAL WILDEBEEST HERD — 20s 分镜提示词包

成片：`output/THE_DIGITAL_WILDEBEEST_HERD_1080p.mp4`  
生成模型：seedance-2.5（text-to-video，原生 720P / 24fps，后期升采样至 1080P）  
结构：**5 段 × 4.0 秒，硬切**，严格对齐原稿 5 个节拍。

> 说明：所有分镜都**不在提示词里要求出现文字**。AI 视频模型渲染英文字母极易糊成乱码，  
> 所以 `PUMP`、两句标语和片名全部由后期图层叠加，保证字形干净可读。

---

## 全局风格锚点（每段都带）

```
cinematic, ultra-realistic wildlife documentary, African savanna, golden hour,
shallow depth of field, long lens, anamorphic flare, heat haze, backlit dust,
4K, 16:9, natural documentary color grade
```

## 全局负向提示词

```
blood, gore, wounds, injury, open wounds, blood splatter, text, letters, words,
subtitles, watermark, logo, cartoon, anime, CGI look, 3D render, humans,
deformed animals, extra limbs, mutated anatomy, low quality
```

---

## Shot 1 · 0:00–0:04 ｜孤独的小角马

> ⚠️ **第一版失败**：提示词里写了 "tiny against the immense landscape"，
> 模型把狮子生成了巨兽，体型约为小角马的 6 倍，比例完全失真。
> 修法：显式规定两者的**屏幕视高比**，并把负向词写死。

```
Ultra-realistic cinematic wildlife documentary, African savanna at golden hour.
In the foreground a young wildebeest calf stands alone on open grassland, tack
sharp, occupying about 45 percent of the frame height, positioned in the lower
centre, head turned to look nervously to one side. Behind it in the mid-ground,
at a realistic distance, a large maned male lion walks slowly and deliberately
toward the calf. The lion is clearly in focus and unmistakably a lion, and its
apparent height on screen is about half the calf's height - a realistic,
physically accurate size relationship, not an exaggerated one. A long stretch of
open grass and heat haze separates the two animals. Low camera at the calf's
shoulder height, long lens compression, golden backlit dust, anamorphic flare,
natural documentary colour grade. Mood: ominous, tense, the quiet before violence.
```

负向词追加：`giant lion, oversized lion, enormous lion, lion as large as the calf,
lion towering over the calf, lion in the foreground, lion close to camera, tiny lion,
indistinct blurry animal, out of focus animal, speck on the horizon`

## Shot 2 · 0:04–0:08 ｜发动攻击

> ⚠️ **第一版失败**：原提示词只写 "lion explodes into a full sprint, charging
> directly toward camera"，结果小角马朝左、狮子朝镜头走，两者节奏接近，
> **读起来像"结伴同行"而不是"追杀"**。
> 修法：改成**侧向追猎**——两者同向奔跑，狮子在角马正后方，且写明
> "the lion is clearly chasing the calf"，负向词排除"并排行走"。

```
Ultra-realistic cinematic wildlife footage, African savanna, golden hour.
A high-speed chase seen side-on. A wildebeest calf gallops at full speed from
left to right across the frame, body fully stretched mid-stride, ears pinned back,
all hooves off the ground, dust spraying up behind it, eyes wide with panic.
A large male lion sprints hard directly behind it, closing the distance, mouth
open, forelegs reaching forward, muscles straining. Both animals run in the same
direction and the lion is clearly chasing the calf. Fast low lateral tracking
camera racing alongside them, motion blur on the grass, dust and debris streaking
past the lens, dramatic golden backlight. Urgent, dangerous, predatory.
```

负向词追加：`animals walking calmly side by side, two animals walking together,
travelling companions, slow walk, stationary animals, calm pacing, relaxed body
language, both animals facing the camera, lion and calf running in parallel`

## Shot 3 · 0:08–0:12 ｜角马群出现

```
Ultra-realistic cinematic wildlife footage, African savanna, golden hour.
Camera rapidly pulls back and rises, revealing the horizon line: hundreds of
wildebeest charging together as one enormous black flood, a living tidal wave of
bodies and dust thundering across the plain toward the lion. The ground vibrates,
dust clouds billow and glow gold in the backlight. In the foreground the small calf
is still running, and the lion hesitates, suddenly uncertain.
Epic wide shot, immense scale, thunderous stampede.
```

## Shot 4 · 0:12–0:16 ｜HERD 反击

```
Ultra-realistic cinematic wildlife footage, African savanna, golden hour.
A vast wildebeest herd crashes into a lone male lion like a tsunami. The lion is
shoved backward, staggers, loses its footing, and is knocked over and swept under
by the immense wall of charging bodies. Camera: violent handheld wide shot from
inside the dust cloud, bodies and hooves streaming past, dust exploding, total
chaos and raw physical impact. Only impact force, dust, and the lion going down.
No blood, no wounds, no injury detail of any kind.
```

## Shot 5 · 0:16–0:20 ｜数字角马群

```
Ultra-realistic cinematic aerial wildlife footage, African savanna at sunset.
Camera rises high into the air and pulls up and away: thousands of wildebeest
running together toward the distant horizon, forming an enormous dark flowing river
of animals across the golden plain, long shadows, glowing dust trails, deep orange
sunset sky. The small calf runs safely in the middle of the herd.
Grand, majestic, triumphant, epic scale, aerial drone documentary.
```

---

## 后期叠加层（不经 AI 生成，保证可读）

| 元素      | 时间码                   | 内容                                          | 处理                                                                         |
| ------- | --------------------- | ------------------------------------------- | -------------------------------------------------------------------------- |
| PUMP 标识 | 00:00.9 – 00:09.2     | 白字红辉光，跟随狮子身体（画布 500×210 / 字号 100px）           | 镜头 1 内贴在狮子胸口、水平微移；硬切后重新落在冲锋的狮子身上；镜头 3 拉远时淡出                               |
| 共用暗带    | 00:12.9 – 00:20.0     | 整幅宽柔和暗底（y 395–670，羽化 105px，峰值 α88）          | 三行文字共用一条，避免各卡自带暗底互相压暗                                                      |
| **第一行** | 出 13.0 ／ 淡出 14.5–15.5 | ONE WILDEBEEST IS WEAK.（y 452，74px）         | **完全清晰 13.34–14.51 = 1.17 秒**                                              |
| **第二行** | 出 14.5 ／ 淡出 16.0–17.0 | THE HERD IS UNSTOPPABLE.（y 620，82px）        | **完全清晰 14.84–16.01 = 1.17 秒**                                              |
| **第三行** | 出 17.0 ／ 保持到结束        | THE DIGITAL WILDEBEEST HERD 🐃（y 536，122px） | **完全清晰 17.34–19.97 = 2.62 秒**                                              |

### 版式规则

- **第一、二行必须分行**：它们在 14.5–15.5 秒有一段交叉溶解（第一行淡出、第二行淡入），  
  同时出现在画面上，所以固定在 y 452 和 y 620 两个不同行。
- **第三行可以占同一块位置**：它和第二行在时间上完全不重叠（第二行 17.0 秒已完全消失），  
  所以直接放在两行块的正中 y 536，字号放大到 122px（两侧金线相应缩短到 66px 让位）。
- 三行都用 4px 黑描边 + 金色辉光，保证压在尘土/夕阳上也能读。

实测（逐帧统计文字区域近白像素，`min(R,G,B) > 195`，取 ≥95% 峰值区间）：

```
L1  ONE WILDEBEEST IS WEAK.           13.34s - 14.51s   1.17s
L2  THE HERD IS UNSTOPPABLE.          14.84s - 16.01s   1.17s
L3  THE DIGITAL WILDEBEEST HERD       17.34s - 19.97s   2.62s   <- 保持到最后一帧
```

### 踩过的坑

- **各卡自带暗底会互相压暗。** 早先每张卡各带一个椭圆暗底（`ry=142` + 165px 模糊），  
  而两行只相距 138px —— 下行的暗底向上蔓延，把上行的白字压灰。  
  实测上行"完全清晰"时长只有 0.00 秒。→ 改为**整幅宽的共用暗带** + 4px 黑描边。
- **验证可读时长必须用像素统计，不能靠肉眼估。** 做法：`ffmpeg -vf fps=24,scale=960:540`  
  逐帧导出 → 统计文字行区域内近白像素数 → 取 ≥95% 峰值的连续区间。
- **颗粒会让统计抖动。** `noise` 滤镜在叠加层之后施加，少量白像素会跌破严格阈值，  
  所以阈值取 `min(R,G,B) > 195` 而不是 225。
- **不要凭缩略图猜主体坐标。** PUMP 标识第一版按想象放在画面上方，  
  实际抽帧后狮子在画面下方。定位前必须先抽帧量真实坐标。
- **重出镜头后必须重算叠加层。** 重做镜头 1、2 之后狮子的位置和大小全变了：
  PUMP 的跟随轨迹要重新量，标识尺寸也要跟着缩小（620×260 / 128px → 500×210 / 100px），
  否则会变成压在狮子脸上的一行大字。
- **交付给预览器的文件，码率按"能被加载"定，不按归档质量定。** 1080p/20s 的社交用途
  4–6 Mbps 足够；44 MB 那次直接导致内置预览器报"编码格式不支持"。
  **胶片颗粒是码率黑洞**（`noise=alls=4` 让 20 秒 1080p 顶到 44 MB），
  想加颗粒就得同时压低 CRF。

> **与原稿的一处偏差**：原稿写「PUMP 字样随着狮子倒地消失（12s）」。  
> 实际渲染后，镜头 3（8–12s）画面里狮子已被尘土遮住、主体是拉远的角马洪流，  
> 标识继续悬浮会变成无主的飘字。所以改为在 8.2–9.2s 淡出 ——  
> 语义上也更顺：角马群一出现，PUMP 的压迫感就散了。

## 声音设计

- **00–08s 低沉紧张**：D2 低音持续音 + 心跳脉冲（0.5s 起逐渐加快）+ 草原风声 + 高频弦状微光
- **08–12s 鼓点渐强**：底鼓间隔从 0.50s 按 0.90 系数递减到 0.17s（加速感）+ 上行 riser
- **12–16s 史诗高潮**：D 小调 braam 叠层（D2/D3/F3 三度错位起音）+ 每 0.5s 重击 + 铜管式和声垫
- **16–20s 收尾**：和声垫延音 → 18.45s 一记 sub boom → 奔跑蹄声与风声渐远

配乐为程序化合成（`assets/audio/make_music.py`），与模型生成的环境音混合。
