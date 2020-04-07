# pure-javascript-i18n Template

Demo: https://cscolabear.github.io/pure-javascript-i18n/

![screencapture-cscolabear-github-io-pure-javascript-i18n-2020-04-07-17_08_42](https://user-images.githubusercontent.com/4863629/78651532-084ef600-78f3-11ea-872f-0f319c40402a.png)


- 使用 HTMLElement.dataset 設定多國語言標籤

e.g.
```html
<h1 data-i18n="title">my title</h1>
.
.
.
<li class="text-center">
    <a href="#article_01" data-i18n="menu_project_overview">Project Overview</a>
</li>
```
- `data-i18n` 內指定語言標籤 `title`
- `data-i18n` 內指定語言標籤 `menu_project_overview`


### js/lang/*.js

在指定語系檔內，設定語言內容

e.g. `js/lang/jp.js`
```javascript
const i18nLangs = {
    title: '私のタイトル',
    .
    .
    .
    menu_project_overview: 'プロジェクト概要',
```


### js/i18n.js

依需求調整 `js/i18n.js` 內參數
```javascript
const i18n = {
    allowLang: ["tw", "jp"],
    defaultLang: "", // 輸入 "tw" 或留空使用 html 上既有內容
    langPath: "./js/lang/",
    .
    .
    .
```
