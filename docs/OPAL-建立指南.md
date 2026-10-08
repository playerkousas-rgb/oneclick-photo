# 🅾️ Google Opal 建立指南 —「一鍵換角度」迷你 App

> 目標:做出一個網頁 App,用戶只要 **上載相 → 揀選項 → 撳一個掣**,Gemini 就會用返佢自己嘅樣貌出圖。
> **完全免費、唔使 API Key、用 Gmail 登入就得、可以分享連結畀朋友**(同你貼嗰個 `spedmix.pages.dev` 一樣嘅形式)。

---

## 一、Opal 係咩?(同你嘅需求有咩關係)

| 項目 | 內容 |
|---|---|
| 係咩 | Google Labs 出品嘅 **免程式碼 AI 迷你 App 產生器**,背後用 Gemini / Imagen |
| 費用 | **免費**(實驗階段,Google 未公佈收費) |
| 要唔要 Key | ❌ 唔使。用 **Google / Gmail 帳號登入**就用得 |
| 出圖方式 | User input(可以係**相片**)→ Generate(Gemini/Imagen)→ Output(網頁顯示圖片) |
| 分享 | ✅ 撳 Publish 就有 **Google 托管嘅分享連結**,對方用自己 Google 帳號就開得 |
| 地區 | 2025 年 11 月起由 15 個國家擴展到 **160+ 個國家**,香港一般開得到 |
| 網址 | `opal.withgoogle.com`(Gemini 網頁版亦有入口) |

**點解啱你?** 因為你唔想複製指令 —— Opal 會把「109 條指令」變成 App 入面嘅**下拉選單 / 選項**,用戶只需要撳。

---

## 二、建立步驟(約 5-10 分鐘)

1. 用電腦 Chrome 去 **opal.withgoogle.com** → 用 **Gmail 登入**。
2. 撳 **Create New**(或「Create with AI / 用描述建立」)。
3. 名稱填:**一鍵換角度**。
4. 將下面「第三章」嘅整段描述**貼入去** → 送出。Opal 會自動砌出 workflow(Input → Generate → Output)。
5. 檢查三個節點:
   - **User input 1** → Advanced → Input type 揀 **Image**(相片)
   - **User input 2** → Input type 揀 **Text**(或下拉選項,放入效果名單)
   - **Generate** → 模型揀有**圖像輸出**嘅 Gemini(如果有 Imagen / Gemini image 選項,揀可以「以圖改圖」嗰個),貼上提示詞
   - **Output** → Webpage / Image
6. 撳 **Preview** 試一次:上載一張相 → 揀「黃金時刻」→ 睇下出圖係唔係保留到你嘅樣。
7. 滿意就撳 **Publish** → 複製分享連結 → 貼落你自己嘅網頁/WhatsApp 就得。

> ⚠️ **一定要試「人物一致性」**:第一次 Preview 請用真人相試「黃金時刻」「移除背景」兩個效果,睇下人物有冇走樣。如果 Generate 節點只支援「文字生成圖」而唔支援「以圖改圖」,人物就會唔同樣 —— 咁就唔好用 Opal,改用下面第四章嘅方法。

---

## 三、可以直接複製嘅 App 描述(貼入 Opal)

```
建立一個叫「一鍵換角度」的迷你 App。用戶上載一張自己嘅相,揀一個拍攝效果,App 就用 Gemini 圖像模型,
以嗰張相為基礎生成新相 —— 同一個人、唔同角度/鏡頭/光線/背景。介面用繁體中文(香港用語)。

【輸入 1|相片 (Image)】
提示文字:請上載一張你正面、清晰、光線均勻、單人嘅相片。

【輸入 2|效果選擇 (Text / 下拉選單)】
讓用戶揀以下其中一個效果(顯示中文名即可):
📐 角度:俯瞰動作 overheadaction|角落視角 cornerpov|荷蘭傾斜 dutchangle|單點透視 onepointperspective|
高角度俯拍 highangle|低角度仰拍 lowangle|蟲眼仰視 wormview|鳥瞰視角 birdsview|平視 eyelevel|
全景全身 widefull|主體偏左 toleft|主體偏右 toright
🔭 鏡頭:移軸微縮 tiltshift|極端POV(鞋底) extremepov|魚眼 fisheyepov|人像特寫 closeup|
半身人像 portrait|螺旋透視 spiralperspective|墮天視角 skyfall
💡 光線:黃金時刻 goldenhour|窗光 windowlight|電影感打光 cinematiclight|光影遊戲 shadowplay|
城市散景 citybokeh|剪影視角 silhouettepov|專業人像打光 portraitpro
⚡ 動態:動態模糊 motionblur|凍結動作 freezeaction|行走動感 walkmotion|動作凝結 actionfreeze|
回頭望 turnbacklook|伸手向鏡頭 reachcamera
🖼 構圖:引導線 leadinglines|對稱構圖 symmetryshot|框中框 framewithinframe|前景框 foregroundframe|
消失點 vanishingpoint|反光倒影 reflectionshot|強迫透視 forcedperspective|景深層次 depthlayers
✨ 特效:傳送門 portalshot|分身效果 cloneeffect|迷你世界 microworld|地面倒影 groundreflection|
錯覺鏡頭 illusionshot|史詩視角 epicperspective
🏙 背景:移除背景 removebg|大自然背景 naturebackground|純色棚 studiobackground|城市天際線 citybackground|
豪華別墅 luxurybackground|極簡背景 minimalbackground|背景虛化 blurbackground|透明背景 transparentbg
🎨 色彩:電影色調 cinematiccolor|青橙 tealorange|黑白 bwportrait|復古 vintagecolor|
暖色 warmcolor|冷色 coolcolor|鮮豔 vibrantcolor
📸 風格:專業形象照 professional|電影感 cinematic|攝影棚 studio|時裝 fashion|奢華 luxury|超寫實 photorealistic

【輸入 3|額外要求 (Text,可留空)】
例如:加笑容 / 換成黑色西裝 / 背景加落雨

【生成 (Generate,用 Gemini 圖像模型)】
以用戶上載嘅相片做「圖像編輯」,唔係由零生成。提示詞:
「Edit the uploaded photo, do not generate a new person.
IDENTITY LOCK:keep the exact same individual — same face, facial features, face shape, skin tone, hairstyle,
hair colour, facial hair, glasses, body proportions, age and outfit. Do not beautify, slim, age or replace them.
No extra people. By default only change camera angle, lens, lighting or colour grade, and keep the original
scene and background as much as possible; only if the chosen effect is a background / VFX / colour / style
effect may you restage the scene, and even then the person must stay identical.
Apply this effect: [用戶揀嘅效果 — 按下面對應表執行].
Additional request from the user: [輸入 3].
Photorealistic professional photography, natural light, correct anatomy, normal hands, sharp focus.」

效果對應指示:
· overheadaction = dramatic high camera angle above the subject looking down, subject tilts head up toward lens
· cornerpov = high camera placed in the corner where two walls meet, shooting diagonally down
· dutchangle = camera tilted 20-30 degrees, close in, subject leans toward lens
· onepointperspective = subject walking centre of a symmetrical corridor, lines converging behind them
· highangle = camera above eye level looking down 30-40 degrees
· lowangle = camera below waist looking up, heroic
· wormview = camera on the ground pointing up, exaggerated perspective
· birdsview / droneview = high top-down view showing the ground and surroundings
· tiltshift = miniature effect, only a thin horizontal band in focus
· fisheyepov = fisheye lens looking straight down at the person
· closeup = tight head-and-shoulders, shallow depth of field
· goldenhour = warm low sun backlight, glowing rim light, sunset tones
· windowlight = soft natural side light from a large window
· cinematiclight = low-key film lighting, deep dark background, contrast on the face
· shadowplay = hard light through blinds casting striped shadows
· citybokeh = night city bokeh lights behind a sharp subject
· silhouettepov = backlit silhouette against a bright sunset sky
· portraitpro = professional studio portrait lighting, clean grey background
· motionblur = background streaked into light trails while the face stays sharp
· freezeaction = high-speed freeze frame, object suspended mid-air
· leadinglines = environmental lines converging toward the subject
· symmetryshot = perfectly symmetrical centred composition
· framewithinframe = subject framed inside a doorway or window
· foregroundframe = shooting through blurred foreground leaves or objects
· reflectionshot = subject together with their reflection in mirror or glass
· forcedperspective = giant hand in the foreground pinching a tiny subject behind
· removebg = remove the background onto a clean neutral studio backdrop
· naturebackground = replace background with lake, mountains and forest
· citybackground = replace background with a modern city skyline
· luxurybackground = luxury villa infinity pool at golden hour
· transparentbg = cut the subject out onto a fully transparent background (PNG)
· tealorange = classic Hollywood teal and orange grade
· bwportrait = high-contrast black and white
· professional = clean business headshot, seamless light background
· cinematic = movie-still look, dramatic lighting, epic location
· photorealistic = hyper-realistic skin texture and real-world lighting
若用戶揀嘅效果唔在上述對應表,用你對該攝影名詞嘅專業理解執行,並保持人物一致。

【輸出 (Output)】
顯示生成嘅相片(大圖),附「下載」同「再試另一個效果」按鈕。全個介面用繁體中文(香港用語)。
```

---

## 四、如果 Opal 唔得點算?(三個後備方案,全部免 Key)

| 方案 | 做法 | 適合 |
|---|---|---|
| **Chrome 擴充功能**(最接近「撳一下就得」) | 下載 `一鍵換角度-擴充功能.zip` → 解壓 → Chrome 去 `chrome://extensions` → 開「開發人員模式」→「載入未封裝項目」→ 揀嗰個資料夾。之後喺 Gemini 上載相 → 撳擴充功能圖示 → 揀效果 → **自動幫你打入去並送出** | 電腦 Chrome 用戶 |
| **Gem + 效果編號** | 用 `GEM-系統指令.txt` 整一個 Gem,之後只需要打「5」或者「/goldenhour」 | 已經整開 Gem |
| **快速指令框** | 喺 `photo-angle-gem.html` 撳效果 → 指令自動填入並全選 → Ctrl+C → 貼落 Gemini | 任何裝置,零安裝 |

---

## 五、注意事項

- **免費額度**:Gemini 免費帳號每日圖片生成有上限(Google 曾公佈約 20 張/日,之後冇再公佈,亦可能隨時調整)。
- **水印**:免費用 Gemini 出圖會有可見水印 + SynthID 標記。
- **Opal 分享**:Publish 之後嘅連結同你 Google Drive 檔案綁定;Google 提醒分享內容可能被收件者看到,唔好放入私人資料。
- **地區/年齡**:Opal 覆蓋 160+ 國家,但仍有機會因帳號類型或年齡限制而開唔到;開唔到就用第四章嘅後備方案。
- **人物一致性**:任何方案都要用「以圖改圖」嘅模型先保得到樣;第一次試請用真人相驗證。
