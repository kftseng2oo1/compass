# 拍照羅盤

結合相機、羅盤、GPS 與水平儀：拍照時把方位角、座標、地址、傾角直接印在照片上，並可匯出 PDF 報告。

**線上使用**：https://kftseng2oo1.github.io/compass/

## 主要功能
- 即時羅盤：轉盤／指針兩種模式、方位刻度帶，支援手動轉動
- 相機畫面疊加方向資訊；拍照時印上方位、時間、經緯度（十進位或度分秒）、海拔、精度
- GPS 反查地址（OpenStreetMap Nominatim）
- 水平儀與拍攝姿勢判斷（俯視／平視／斜視）
- 每張照片可加備註；相片庫可預覽、下載、刪除
- 一鍵產生 PDF 報告並透過分享選單傳出
- 磁場干擾、指針卡住時提示 ∞ 字形校正；拍攝時保持螢幕常亮

## 使用方式
1. 必須用 HTTPS 開啟（GitHub Pages 即可），`file://` 無法使用相機與感測器
2. 按「啟動」並允許相機、位置、動態感測權限（iOS 需在 Safari 設定開啟「動態與健身」）
3. 對準目標拍照，到「📷 相片庫」查看或按「📄 報告」匯出

## 技術與依賴
- 單檔 HTML PWA（`index.html` 內含全部 HTML/CSS/JS），`manifest.json` + `sw.js` 提供安裝到主畫面與離線快取。
- `DeviceOrientation`、`getUserMedia`、`geolocation`、Wake Lock、Web Share
- PDF 由 jsPDF（cdnjs）產生；地址查詢需連網
