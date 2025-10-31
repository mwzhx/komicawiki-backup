# KomicaWiki-Backup

This is a repository for backup files of Komica Wiki.

## index-browser 網頁搜尋與復原條目

 1. 開啟 [index-browser 網頁][index-browser] (流量約 2MB)

 2. 在搜尋欄輸入關鍵字以列出標題符合的條目

 3. preview 按鈕會在新分頁開啟條目，
    github 連結會連到該檔案在 github 上的頁面，
    html 連結可以檢視原始碼或右鍵另存新檔。

 4. 也可以用正則表示式搜尋 (regular expression)

 5. **clean html** 按鈕可以複製清理過的 html，直接貼到 pandoc 轉換的結果較乾淨。

 6. **copy wiki** 按鈕會直接在瀏覽器內調用網頁版 (wasm) pandoc 轉換，轉換完的成果更乾淨；但會用掉約 10MB 的流量來載入 pandoc。轉換完會將結果顯示在下方的文字框中並複製，偶爾會複製失敗，手動在文字框中全選複製即可。

 7. 如果您有自己備份或從 web.archive.org 抓來的 html 檔案，也可以拖曳檔案到文字框內、用瀏覽按鈕載入檔案、直接貼上整個網頁的 html 原始碼到文字框中，再按下 **html to wiki** 的按鈕，即可轉換為 wiki 語法。

[index-browser]: https://mwzhx.github.io/komicawiki-backup/index-browser.html

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
