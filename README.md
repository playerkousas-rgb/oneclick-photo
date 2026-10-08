# 📷 一鍵換角度 — AI 攝影師(網站)

上載一張自己嘅相,揀一個效果(109 個),Gemini 就生成**同一個人、唔同角度/鏡頭/光線/背景**嘅專業相。
唔使 API Key、唔使伺服器、唔使後台 —— 純靜態網站 + 一個 Gemini Gem。

---

## 📁 檔案結構

```
index.html          ← 首頁(門面,有大按鈕連去你嘅 Gem)★ 主要入口
tool.html           ← 109 個效果目錄(工作台,支援複製指令 / 打編號)
lite.html           ← 輕量版(冇示範圖,檔案細,慢網絡備用)
docs/               ← 指令檔同說明(唔影響網站運作,可以直接刪)
  GEM-系統指令.txt         Gem 嘅系統指令(長版)
  GEM-系統指令-短版.txt    短版,如果長版貼唔入就用呢個
  效果指令大全.txt         109 條完整指令(可列印)
  使用說明.md              完整操作說明
  OPAL-建立指南.md         用 Google Opal 做迷你 App 嘅方法
extra/
  extension.zip            Chrome 擴充功能(撳效果自動打入 Gemini)
  api.html                進階:用 API Key 一撳即出圖版本
```

---

## 🚀 部署到 Vercel(3 分鐘)

### 第一步:放上 GitHub
**方法 A(網頁上傳,最簡單)**
1. 去 [github.com/new](https://github.com/new) → Repository name 填 `oneclick-photo` → **Public** → Create。
2. 撳 **uploading an existing file** → 將**解壓後全部檔案同資料夾**拖入去(包括 `docs/`、`extra/`)。
3. 撳 **Commit changes**。

**方法 B(用 Git 指令)**
```bash
git init
git add .
git commit -m "一鍵換角度網站"
git branch -M main
git remote add origin https://github.com/你的帳號/oneclick-photo.git
git push -u origin main
```

### 第二步:部署 Vercel
1. 去 [vercel.com](https://vercel.com) → **Sign up with GitHub**(授權一次)。
2. 撳 **Add New… → Project** → 揀你頭先個 repo → **Import**。
3. 設定(**照住填**):
   - Framework Preset: **Other**
   - Build Command: **留空**
   - Output Directory: **留空**
   - Root Directory: **留空**
4. 撳 **Deploy** → 等 20 秒 → 完成 ✅ 你會得到 `https://你的專案.vercel.app`

> 之後每次改完檔案再 push 上 GitHub,Vercel 會**自動重新部署**。

### 第三步:試一試
1. 開 `https://你的專案.vercel.app`
2. 撳首頁大按鈕 → 應該開你嘅 Gemini Gem
3. 喺 Gemini 上載相 → 打編號(例如 `52`)→ 出圖

---

## 🔧 想更換 Gem 連結?

改兩個檔案入面嗰句就得(用文字編輯器搵 `gemini.google.com/gem/`):

| 檔案 | 位置 |
|---|---|
| `index.html` | 搜尋 `__GEM__` 或 `gemini.google.com/gem/`(會有兩處:頂部按鈕 + 底部浮動按鈕) |
| `tool.html` | 搜尋 `GEM_LINK_DEFAULT` |

---

## 💡 常見問題

**Q:要唔要畀錢?** 唔使。Vercel 免費額度對呢種靜態網站完全夠用(個人專案免費)。
**Q:會唔會收我 API 費用?** 唔會,呢個網站冇 API Key。出圖係用訪客自己嘅 Google 帳號 + Gemini 免費額度。
**Q:Gem 分享設定要注意?** Gem 一定要設做「**任何人擁有連結**」,否則訪客撳入去會話冇權限。
**Q:朋友需要畀錢嗎?** 唔需要,用免費 Google 帳號就得(每日有圖片生成上限,Google 曾公佈約 20 張/日,之後未再公佈,亦可能調整)。
**Q:想用 GitHub Pages?** 都可以:Repo → Settings → Pages → Source 揀 `main` / `root` → Save。網址會係 `https://你的帳號.github.io/oneclick-photo/`。

---

## ⚠️ 請注意

- 唔好將任何私人資料(API Key、密碼)放入呢個資料夾 —— 上到 GitHub 就係公開。
- 相片由 Google Gemini 生成,免費版可能附有可見水印及 SynthID 隱形標記。
- 呢個網站只係門面 + 目錄,實際運算全部喺 Google Gemini 進行。
