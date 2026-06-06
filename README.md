# Macau-High-school-students-Python-Problem-Exercise
澳門中學生Python解難大賽歷屆真題練習

## 模擬測試系統

以單檔 HTML 製作，直接用瀏覽器開啟即可使用，無需安裝。

- **`Python-Competition-Practise-v2.html`（最新版，推薦）** — 全面重寫版本：
  - 現代化介面、深 / 淺色主題切換、作答進度條與計時。
  - **按賽段（初賽 / 決賽）與屆數篩選**題目。
  - 多種練習模式：全部題目、只練選擇題、只練程式 / 簡答題、**錯題重練**、**我的收藏**。
  - 可選作答時限（到時自動交卷）、題目隨機或依原順序。
  - 自動以瀏覽器 `localStorage` 暫存作答進度（可續答）、記錄錯題本與收藏。
  - 交卷後提供逐題解析：對 / 錯標示、正確答案、知識點與解題思路。
- `Python-Competition-Practise-v1.html` — 初版（保留作參考）。

## 如何新增題目 / 新一屆試題

題庫資料就在 v2 檔案的 `<script>` 區塊（`preliminaryChoice`、`preliminaryText`、`finalChoice`、`finalText`）。
每題的 `edition` 欄位為**選填**，標上即可在首頁「屆數」下拉中篩選；未標的題目會歸入「歷屆綜合題」。

```js
// 選擇題
{ edition: "第四屆", question: "題目…", options: ["A","B","C","D"], answerIndex: 0,
  knowledge_points: "知識點", solution_idea: "解題思路" }

// 程式結果題 / 簡答題
{ edition: "第四屆", type: "text", question: "題目（可含 <code>程式碼</code>）",
  answer: "參考答案", knowledge_points: "知識點", solution_idea: "解題思路" }
```

題目字串開頭的題號（如 `12.`、`簡答題 2：`）會被系統自動清除並重新編號，照抄原卷即可。

## 比賽資訊與資料來源

題目整理自澳門生產力暨科技轉移中心（CPTTM）「全澳中學生 Python 解難大賽」歷屆真題。
初賽形式：60 分鐘、全卷 100 分、以 Python 3 為準；範圍涵蓋基礎語法、資料結構、檔案處理、
list comprehension、lambda / map、生成器 / 迭代器、OOP 與 dunder methods、numpy / pandas / matplotlib、爬蟲與 XML 解析等。

- [CPTTM 官網 · 全澳中學生 Python 解難大賽](https://www.cpttm.org.mo/ist/it-competitions/python-competition/)
- [第五屆報名頁（2025）](https://events.cpttm.org.mo/competition/226?l=c)
- [第三屆比賽頁（含初賽真題 PDF）](https://www.cpttm.org.mo/ist/it-competitions/python-competition/3rd/)
- [政府新聞稿 · 比賽圓滿舉行](https://www.gov.mo/zh-hant/news/1151194/)

> 註：官方僅公開部分屆別的初賽試題（如第三屆初賽真題 PDF），第四 / 五屆完整試卷未公開下載。
> 截至最後更新，第六屆（2026）尚未見官方公告，請以官網最新資訊為準。
