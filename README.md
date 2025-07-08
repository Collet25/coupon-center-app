# 優惠券系統 Coupon Center App

## 專案簡介

本專案為我在大專專題中負責開發的前台優惠券系統，主要功能為提供會員登入後可領取、收藏優惠券，並加入每日挑戰遊戲等互動機制，模擬實際博物館會員活動的使用情境。

我主要負責的部分包括：
- 優惠券列表頁的設計與資料渲染
- 領券按鈕功能（單張領取 / 一鍵領取）
- 登入狀態下的條件渲染
- 每日挑戰小遊戲設計與串接 API 發券
- 收藏按鈕功能、提示 modal 與狀態處理

>  此版本為我個人獨立整理與重構的作品集版本，非完整團隊原始碼。

## 使用技術
- React.js (Next.js 框架)
- Bootstrap & SCSS
- Node.js + Express（後端 API）
- MySQL（會員 / 優惠券 / 收藏資料）
- Axios（前後端串接）
- React Router / useParams / useEffect / useState

## 主要功能
- 顯示所有優惠券列表（未登入也可瀏覽）
- 判斷會員登入狀態，自動切換 UI 顯示
- 領取功能（單張領取 / 一鍵領券）
- 每日挑戰成功後自動領取特定優惠券
- 已領取／未領取優惠券分頁與提示

## 專案啟動方式

### 1. Clone 專案

```bash
git clone https://github.com/Collet25/exhibition-coupon-app.git
cd exhibition-coupon-app

### 2. 安裝前後端依賴
# 前端
cd client
npm install

# 後端
cd ../backend
npm install

### 3. 設定環境變數
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=你的密碼
DB_NAME=museum
PORT=3005

### 4. 匯入資料庫（MySQL）

先建立資料庫 `museum`，接著匯入以下 SQL：

```bash
# 匯入資料表結構
mysql -u root -p museum < backend/database/database.sql

### 5. 啟動伺服器與前端

```bash
# 啟動後端
cd backend
npm run dev

# 啟動前端
cd ../client
npm run dev

預設前端會在 http://localhost:3000 開啟，後端則在 http://localhost:3005

## 測試帳號

| 角色   | 帳號              | 密碼     |
|--------|-------------------|----------|
| 測試會員 | test1@test.com    | 12345Ab@  |

> 登入後可測試：
> - 領取優惠券（單張 / 一鍵）
> - 每日挑戰領券
> - 收藏功能與分頁篩選

