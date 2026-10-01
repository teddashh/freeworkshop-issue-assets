# freeworkshop-issue-assets

[English](README.md) · **繁體中文**

自由工坊 Discord 小幫手 bot 代社群成員開立 GitHub issue 時，附上的截圖都存在這裡。

**專案介紹頁：** https://teddashh.github.io/freeworkshop-issue-assets/?lang=zh-TW

有人在自由工坊 Discord 回報問題時，小幫手 bot 會先擬好 GitHub issue 草稿。回報者或管理員在 Discord 確認草稿之後，bot 才會開立 issue，把附上的截圖提交到這個 repo，再在 issue 裡附上連結。Discord CDN 的附件連結會過期，所以圖片需要一個固定的存放位置。

## 路徑規則

```
<owner>/<repo>/<YYYY-MM>/<draft-id>-<n>.<ext>
```

- `<owner>/<repo>`：issue 所在的 repo
- `<YYYY-MM>`：年份與月份
- `<draft-id>`：Discord 草稿編號
- `<n>`：這份草稿裡的第幾張截圖

issue 透過 `main` 分支的 `raw.githubusercontent.com` 網址連結到這些檔案。

## 隱私

- 上傳前會先移除中繼資料（EXIF）。
- 這個 repo 是公開的，草稿一經確認，截圖也就公開了。確認之前，請先看清楚截圖裡有什麼。
- 專案介紹頁只用 `site/` 建置，不會發佈存放的圖片。

## 移除圖片

如果截圖拍到個人資料或機密資訊：

1. 如果畫面上看得到密碼、token 或金鑰，請先更換。刪掉圖片並不能讓外洩的資訊收回來。
2. 在自由工坊 Discord 找管理員；不在 Discord 的話，就在這個 repo 開 issue。寫出是哪個 issue、第幾張截圖，或檔案路徑就好，不要再附一次圖片。
3. 維護者會刪除這裡的檔案，並編輯 issue 拿掉連結。

從 `main` 刪除檔案後，issue 裡的圖片連結就會失效；但在改寫 Git 歷史之前，舊的 commit 裡仍然留有這個檔案。

## 這個 repo 裡有什麼

只有圖片，bot 的程式碼不在這裡。`site/` 與 `.github/workflows/pages.yml` 用來建置專案介紹頁。
