# KomicaWiki-Backup

This is a repository for backup files of Komica Wiki.

## index-browser 網頁搜尋

 1. 開啟 [index-browser 網頁][index-browser]

 2. 在搜尋欄輸入關鍵字以列出標題符合的條目

 3. preview 按鈕會在新分頁開啟條目，
    github 連結會連到該檔案在 github 上的頁面，
    html 連結可以檢視原始碼或右鍵另存新檔。

 4. 也可以用正則表示式搜尋 (regular expression)

[index-browser]: https://mwzhx.github.io/komicawiki-backup/index-browser.html

## github 搜尋檔案

鑑於 github 關閉訪客搜尋功能，本方法需要登入 github 才能使用

 1. 在搜尋欄輸入想尋找條目備份檔的條目名稱

    ![搜尋欄](https://user-images.githubusercontent.com/13307281/208006290-c7f10d46-d03d-4b23-a8b2-8369a1dd6962.png)

 2. 選擇 (search) in this repository 的搜尋建議

    ![在本倉庫中搜尋](https://user-images.githubusercontent.com/13307281/208006495-e1e67040-91c0-4905-80d3-05a58a6a99ed.png)

 3. 找出你覺得內容最多的條目。例如尾綴數字可能是重覆的內容，討論、投票頁不含有主要內容的可以略過。
    點擊檔名標題可以進入該檔案頁面。

    ![搜尋結果](https://user-images.githubusercontent.com/13307281/208006801-9e32200f-9248-461d-bab4-bb940ce61212.png)

 4. 在右上方的 Raw 按鈕上按右鍵，選擇鏈結另存新檔，以下載原始檔案。

    ![另存新檔](https://user-images.githubusercontent.com/13307281/208007911-2f08b369-73dc-468f-9dd9-7c7c11a8cd7d.png)

## html 格式備份
html 檔案原則上可以雙擊後直接在瀏覽器打開，若要自動轉換為 media wiki 格式文字，
可以使用 [pandoc] 或 [free file convert] 進行轉換，但二者皆無法完整轉換，
例如無法轉換回模板原始碼，轉換後的 media wiki 文字也會包含大量無法轉換的 html 原始碼。

[pandoc]: https://pandoc.org/
[free file convert]: https://www.freefileconvert.com/document-converter

### pandoc 轉換教學

 1. 進入 [pandoc 網頁版](https://pandoc.org/try/)

 2. 格式選擇 from `html` to `mediawiki`

    ![格式 from html to mediawiki](https://user-images.githubusercontent.com/13307281/216226398-2ad111c8-8d0f-45c1-a404-682d4dffab33.png)

 3. 用 *瀏覽* 選取 html 檔案或是直接將 html 原始碼貼入文字框中

 4. 點擊 `Convert` 按鈕，轉換結果即會在右側顯示。若有無法轉換的內容，會用綠色訊息顯示，其他轉換內容則會顯示在下方。

### free file convert 轉換教學

 1. 點擊 [free file convert 網站][free file convert] 中的 File 頁籤

    ![file 頁籤](https://user-images.githubusercontent.com/13307281/208011773-dd3fbe0a-68b2-4428-a908-e892f480eb6f.png)

 2. 選擇檔案，並將 output format 設為 wiki，後點擊右側步驟 3 的藍色 Convert 按鈕

    ![output format wiki](https://user-images.githubusercontent.com/13307281/208012216-7e25eb68-3236-445a-b610-dde2a91f1589.png)

 3. 轉換成功後，點擊 download 按鈕下載

    ![downlaod 按鈕](https://user-images.githubusercontent.com/13307281/208012419-f04032bf-4567-44d4-8bcb-162efa9a09f7.png)

### 轉換內容說明
轉換後的 wiki 格式檔案內容多半會混雜大量 html 在 wiki 語法內。
以下範例開頭部份為 google 頁庫存檔說明無法轉換，
後面有部份轉換成功的 wiki 內容。

```wiki
<div id="bN015htcoyT__google-cache-hdr">

<div>

<span>這是 Google 對 https://wiki.komica.org/index.php?title=%E5%8D%81%E9%87%8C%E5%9D%A1%E5%8A%8D%E7%A5%9E&mobileaction=toggle_view_desktop 的快取。</span> <span>這是該網頁於 2022 年 10 月 25 日 15:17:52 GMT 顯示時的快照。</span> <span>在此期間，[https://wiki.komica.org/index.php?title=%E5%8D%81%E9%87%8C%E5%9D%A1%E5%8A%8D%E7%A5%9E&mobileaction=toggle_view_desktop 目前網頁]可能已經變更。</span> [http://support.google.com/websearch/bin/answer.py?hl=zh-TW&p=cached&answer=1687222 <span>瞭解更多資訊</span>.]

</div>
<div>

<span style="display:inline-block;margin-top:8px;margin-right:104px;white-space:nowrap"><span style="margin-right:28px"><span style="font-weight:bold">完整版</span></span><span style="margin-right:28px">[http://webcache.googleusercontent.com/search?q=cache:yjN07AdoIOcJ:https://wiki.komica.org/index.php?title%3D%25E5%258D%2581%25E9%2587%258C%25E5%259D%25A1%25E5%258A%258D%25E7%25A5%259E%26mobileaction%3Dtoggle_view_desktop&hl=zh-TW&gl=tw&strip=1&vwsrc=0 <span>純文字版</span>]</span><span style="margin-right:28px">[http://webcache.googleusercontent.com/search?q=cache:yjN07AdoIOcJ:https://wiki.komica.org/index.php?title%3D%25E5%258D%2581%25E9%2587%258C%25E5%259D%25A1%25E5%258A%258D%25E7%25A5%259E%26mobileaction%3Dtoggle_view_desktop&hl=zh-TW&gl=tw&strip=0&vwsrc=1 <span>檢視原始碼</span>]</span></span>

</div>
<span style="display:inline-block;margin-top:8px;color:#70757a"><span>提示：如要在這個網頁上快速尋找您所搜尋的字詞，請按下 '''Ctrl+F''' 鍵或 '''⌘-F''' 鍵 (Mac)，然後使用尋找列進行搜尋。</span></span>

</div>
<div style="position:relative;">

<div id="mw-page-base" class="noprint">



</div>
<div id="mw-head-base" class="noprint">



</div>
<div id="content" class="mw-body" role="main">

[[|]]
<div id="siteNotice" class="mw-body-content">

<div id="localNotice" lang="zh-Hant-TW" dir="ltr">

<div class="mw-parser-output">

{|
!width="100%"| <span style="font-size:22px;">公告</span>
|-
| <span style="font-size:10px;">更新日期：2022/02/06</span>
|-
|
因應近日 KomicaWiki 遭惡意使用者嚴重攻擊，為了減少傷害故啟用封鎖政策。對影響到其他使用者深感抱歉。當前'''僅許可'''「'''已註冊用戶'''」編輯，並暫停新用戶使用系統註冊的申請。
如有不便，敬請見諒。
|}
```

### 換行符轉換
從 free file convert 下載的 wiki 檔案，多半是使用 `LF` (`\n`) 作為 [換行符]，
如果在 windows 用記事本打開，
會因為 windows 不認得 `LF` 作為換行符，
造成換行符消失而所有行擠在同一行。

[換行符]: https://zh.wikipedia.org/wiki/%E6%8F%9B%E8%A1%8C

要讓換行符恢復正常換行，可以使用 [此線上 markdown 編輯器][md] 的載入檔案功能：
選擇工具列的 *Upload File* > *Upload File from Computer* ，
載入先前下載的 wiki 檔案，wiki 文字即可正常顯示在編輯器中。
隨後使用 *Download File* 按鈕或是複製貼上到記事本皆可。

[md]: https://www.tutorialspoint.com/online_markdown_editor.php


## Contributing

This repository require linear history. Do NOT create merge commits.

### web 分支編輯教學
web 分支是 github-page 用的分支，
是用 [特殊方式][orphan] 建立的分支，
和 master 分支沒有共同的祖先。

[orphan]: https://stackoverflow.com/a/1384723

直接 switch 時 komicawiki-backup repo 裡海量的檔案會淹死你，
要編輯的話建議可以另外 clone 在新的目錄，

```sh
git clone --single-branch --branch web \
    https://github.com/mwzhx/komicawiki-backup \
    komicawiki-backup-web
```

或用 worktree

```sh
git branch web origin/web
git worktree add web
cd web
git log
```
