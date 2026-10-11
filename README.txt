Ledgerly 部署說明
==================

這個資料夾是純靜態網站,不需要後端,整包上傳就能用。

檔案
  index.html            主程式
  manifest.webmanifest  讓網站可以「安裝」成 App
  sw.js                 離線快取(沒網路也能開)
  icon-180/192/512.png  黑底白色 App 圖示(iPhone 用 180)
  favicon-32.png        瀏覽器分頁小圖示

上傳方式(三選一,都免費)
  1. Netlify Drop:到 app.netlify.com/drop,把整個資料夾拖進去,幾秒後拿到網址。
  2. Cloudflare Pages:建立專案 → Direct Upload → 上傳資料夾。
  3. GitHub Pages:建新 repo,把這些檔案放在根目錄,Settings → Pages → 選 main 分支。
  務必使用 HTTPS 網址(以上三個都是),PIN 鎖與離線功能才會正常。

iPhone 加到主畫面
  用 Safari 開啟網址 → 分享按鈕 → 加入主畫面。
  圖示會是黑底白色的 Ledgerly,開啟後是全螢幕、沒有網址列。

重要:資料不會從舊版帶過來
  資料存在「瀏覽器的本機儲存空間」,每個網址各自獨立。
  搬家請先在舊版:設定 → 資料匯出 → 下載 JSON 備份,
  再到新網址:設定 → 資料匯入 → 選 JSON 檔 → 匯入。
  也建議定期備份;iOS 若很久沒開 Safari 可能清掉網站資料,
  加到主畫面使用比較不容易被清掉。

之後要更新
  直接把新的 index.html 覆蓋上傳。若畫面沒更新,把 sw.js 裡的
  ledgerly-v6 改成 ledgerly-v7 再上傳即可。
