# Google Publisher Tag（GPT）

## 顯示廣告單元

***[googletag.display(div)](https://developers.google.com/doubleclick-gpt/reference#googletag.disablePublisherConsole)***

每一個廣告空間應該每一頁只顯示一次，在顯示廣告之前，應先定義好

## 啟用 GPT 服務

***[googletag.enableServices()](https://developers.google.com/doubleclick-gpt/reference#googletag.enableServices)***

## 取得 GPT 版本

***[googletag.getVersion()](https://developers.google.com/doubleclick-gpt/reference#googletag.getVersion)***

## 啟用同步載入

***[googletag.enableSyncLoading()](https://developers.google.com/doubleclick-gpt/reference#googletag.CompanionAdsService_enableSyncLoading)***

同步載入廣告，必須在呼叫 `googletag.enableServices()` 前就呼叫


```html
<div id="div-1" style="width: 728px; height: 90px">
  <script type="text/javascript">
    googletag.cmd.push(function() {
        //  將廣告單元顯示在 div-1
        googletag.display('div-1');
    });
  </script>
</div>
```

## 指定解析度顯示指定廣告大小廣告

***[SizeMappingBuilder](https://developers.google.com/doubleclick-gpt/reference#googletag.SizeMappingBuilder)***

```javascript
googletag.cmd.push(function() {
    var mapping = googletag.sizeMapping().
        // 解析度大於 1024x768 時顯示 970x250 或 970x90 的廣告
        addSize([1024, 768], [[970, 250], [970, 90]]).
        // 解析度大於 980x690 時，顯示 728x90 的廣告
        addSize([980, 690], [728, 90]).
        // 解析度介於 980x690 ~ 750x250 之間時，不顯示任何廣告
        addSize([750, 250], []).
        // 解析度介於 750x250 ~ 320x250 之間時，顯示 300x250 的廣告
        addSize([320, 250], [300, 250]).
        // 解析度介於 320x250 ~ 0x0 之間時，不顯示任何廣告
        addSize([0, 0], []).
        build();

    // 定義使用廣告空間 /123/dfp_slot_name
    // 接受的廣告大小為 320x250, 728x90, 970x90, 970x250
    var slot = googletag.defineSlot('/123/dfp_slot_name', [[300, 250] , [728, 90], [970, 250], [970, 90]], 'dfp_display_div_id')
            .defineSizeMapping(mapping)
            .addService(googletag.pubads());
});
```

## 移除指定廣告空間

***[googletag.destroySlots(opt_slots)](https://developers.google.com/doubleclick-gpt/reference#googletag.destroySlots)***


```javascript
var slot = googletag.defineSlot('/123/dfp_slot_name', [[300, 250] , [728, 90], [970, 250], [970, 90]], 'dfp_display_div_id')
            .defineSizeMapping(mapping)
            .addService(googletag.pubads());

googletag.display('dfp_display_div_id');
// 移除指定廣告空間
googletag.destroySlots([slot1]);
```

## 開啟廣告 console

```javascript
// 透過 div 編號呼叫
googletag.openConsole('div-1');

// 不透過 div 編號呼叫
googletag.openConsole();
```

## 參考資料
* [GPT Reference  |  Google Publisher Tag  |  Google Developers](https://developers.google.com/doubleclick-gpt/reference)