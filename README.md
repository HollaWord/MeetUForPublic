# MeetU: 聚會交友平台

### 專案目的
我們是一群剛開始學習程式設計的學生，這個專案是我們的期末專題。**MeetU** 平台讓用戶可以創建帳號、結交朋友，甚至在線上尋找真愛。我們的目標是，與傳統交友應用相比，讓用戶更容易建立現實生活中的關係。</br>
**MeetU管理後台**：https://github.com/ReynoldCircle/MeetU_backend.git

### 專案成員
[Emerald](https://github.com/HollaWord) , [Benson](https://github.com/chengyu9072) , [Noel](https://github.com/Noelyan1995), [Jayson](https://github.com/jaysonyang503) , [ReynoldYuan](https://github.com/ReynoldCircle)

**MeetU** 包含以下功能：
- **會員創建/修改/註銷，及googole登入**
- **每日隨機配對(目前設定一天上限為3位)**
- **貼文和評論**
- **一對一與群組聊天**
- **追蹤**
- **舉辦/報名/審核/收藏活動等**
- **即時系統通知-對單個用戶或全體用戶**
- **用戶封鎖機制**
- **對用戶、活動及評論可進行檢舉**

### 技術堆疊
- **後端**: Spring Boot
- **前端**: Vue 3
- **資料庫**: Microsoft SQL Server (MSSQL)
- **即時通訊**: WebSocket, polling

# 細節請參閱我們的 MeetU.pptx 和展示影片
因PPT包含影片檔造成檔案較大，請直接於下方網址查看：</br>
https://1drv.ms/p/s!Ark_lrwm9EcYgbFvUlWK7K1gZgVTtw?e=LRsKnx

### 安裝說明
按照以下步驟設置並運行此專案：

1. **更新 MSSQL 配置**：
   在 `application.properties` 文件中，修改 MSSQL 的連接配置，包括port、用戶名和密碼。

2. **更新信箱配置**：
   在 `application.properties` 文件中，修改 spring.mail 的用戶名和密碼配置。<br>
   密碼的部分請去google申請一個應用程式密碼再作輸入，申請位置在我的帳戶 -> 安全性 -> 兩步驟驗證。<br>
   沒有的話請直接搜尋應用程式密碼。

3. **更新google-oauth2.properties配置**：
   請到google developer console建立新專案，建好後設定OAuth同意畫面和申請憑證。<br>
   憑證裡面找到client_id、client_secret和redirect_uris後填入google-oauth2.properties對應的屬性裡。

4. **創建資料庫結構**：
   在 MSSQL 中執行 `data.sql` 腳本，以建立必要的資料表和結構。</br>
   或者可直接使用 `MeetU.bak` 建立預設資料 (請注意,部分圖片可能無法正常顯示，建議直接透過網頁前台做修改)

5. **安裝依賴包**：
   在專案根目錄下運行以下命令以安裝必要的依賴包：
   ```bash
   npm install

6. **啟動開發伺服器**：
   依賴包安裝完成後，使用以下命令啟動開發伺服器：
   ```bash
   npm run dev

# 已知問題
由於時間限制，部分功能僅部分實現。<br>

