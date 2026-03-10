# VD 車輛偵測器分佈地圖 (VD Map)

這是一個簡單的可視化網頁，用來在地圖上標示台灣各地「VD 車輛偵測器」的點位資訊。

## 專案功能
* 透過 [Leaflet](https://leafletjs.com/) 在網頁中嵌入互動式地圖。
* 使用 [PapaParse](https://www.papaparse.com/) 解析 CSV 格式的車輛偵測器資料。
* 提供彈出視窗顯示偵測站詳細資訊（如代碼、所在道路、公里數、車道數等）。

## 網頁連結
點擊這裡查看地圖： **[VD 車輛偵測器分佈地圖](https://Luluboy168.github.io/VD_map/)**

## 資料來源
本專案使用的車輛偵測器 (VD) 原始 XML 資料來源為：
* **[交通部高速公路局 交通資訊蒐集系統 (TISVCloud)](https://tisvcloud.freeway.gov.tw/)**

## 如何在本地執行
因為網頁需要讀取同一個資料夾底下的 `VD_parsed.csv` 資料檔，為了避免瀏覽器發生 CORS（跨來源資源共用）的阻擋，請不要直接點擊兩下 HTML 檔案開啟。
建議透過本地伺服器來執行，例如：
1. 確保已安裝 Python 3
2. 在此資料夾打開終端機，輸入：
   ```bash
   python -m http.server 8000
   ```
3. 打開瀏覽器前往 `http://localhost:8000/`

## 檔案結構
* `index.html`: 主網頁檔（地圖呈現）。
* `VD_parsed.csv`: 已經從 XML 解析出來、帶有經緯度與相關資訊的車輛偵測器點位資料。
* `README.md`: 本說明文件。
