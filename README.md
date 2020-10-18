# Side-Project-GoogleSheets-to-WebDatabase

![alt](/final.png)

<https://github.com/johch3n611u/Side-Project-Try-Some-Electron.net>

繼上次幫老母實作 Electron.net 單機版本的 SheetFilter 後，釐清需求其實比較需要的是 Web System 的 SheetFilter。

就不會有不會安裝或使用的狀況發生，瀏覽器打開網址貼上即可。

所以目前會在此專案記錄過程，實作後會統整在 <https://github.com/Cara-Drumstick-Bug> 當作其中一個可以 demo 的範例。

## 步驟

1. 開啟 Google 共用連結 2.sheet 就是指這個 excel 的第幾張表，一次只能 GET 一張 sheet

   <https://spreadsheets.google.com/feeds/list/{excel_id}/{sheet}/public/values?alt=json>

   ```javascript
    $(function() {
      $.get(
         'https://docs.google.com/spreadsheets/d/{excel_id}/edit#gid=0',
         function(data) {
            console.log(data);
         }
      );
    });
   ```

2. JavaScript Array forEach() Method 抓 item , arr , index

   <https://www.w3schools.com/jsref/jsref_foreach.asp>

3. get keys of json-object in JavaScript [duplicate]

   <https://stackoverflow.com/questions/8430336/get-keys-of-json-object-in-javascript/8430374>

4. JavaScript String includes() Method 比對 資料內有相同的

   <https://www.w3schools.com/jsref/jsref_includes.asp>

5. 整理頁首資料

   <https://www.fooish.com/javascript/object.html>

   <https://expect7.pixnet.net/blog/post/61152064>

   <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace>

6. 取 JSON 動態 key 裡面的資料 Object[KeyName]

   <https://zhidao.baidu.com/question/1930522725913059547>

## 架構

以 GoogleSheets 當作 db ，並利用 GithubPage 實作靜態讀取。

## 參考

<https://letswrite.tw/google-excel-db/>
