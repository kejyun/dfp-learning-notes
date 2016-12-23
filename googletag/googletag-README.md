# Google Publisher Tag

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

## 參考資料
* [GPT Reference  |  Google Publisher Tag  |  Google Developers](https://developers.google.com/doubleclick-gpt/reference)