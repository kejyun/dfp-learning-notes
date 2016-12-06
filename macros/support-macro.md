# 參數

* %%CLICK_URL_UNESC%% : 點擊時 DFP 紀錄廣告統計資料的連結（不要過濾跳脫字元）
* %%CLICK_URL_ESC%% : 點擊時 DFP 紀錄廣告統計資料的連結（過濾跳脫字元 1 次）
* %%CLICK_URL_ESC_ESC%% : 點擊時 DFP 紀錄廣告統計資料的連結（過濾跳脫字元 2 次）
* %%CACHEBUSTER%% : 清除快取隨機變數
* %%WIDTH%% : 廣告寬度
* %%HEIGHT%% : 廣告高度
* %%DEST_URL_UNESC%% : 點擊時 DFP 紀錄廣告統計資料重新導向目標網址（不要過濾跳脫字元）
* %%DEST_URL%% : 點擊時 DFP 紀錄廣告統計資料重新導向目標網址（過濾跳脫字元 1 次）
* %%DEST_URL_ESC%% : 點擊時 DFP 紀錄廣告統計資料重新導向目標網址（過濾跳脫字元 1 次）
* %%DEST_URL_ESC_ESC%% : 點擊時 DFP 紀錄廣告統計資料重新導向目標網址（過濾跳脫字元 2 次）
* %%PATTERN:key%% : 模式比對巨集(鍵值)
* %%PATTERN:TARGETINGMAP%% : 模式比對巨集(鍵值物件)
* %%PATTERN:url%% : 模式比對巨集(網址)
* %%TARGET_IN_NEW_WINDOW%% : 在新視窗中開啟目標巨集
* %%TARGET_WINDOW%% : 目標視窗巨集
* %%TFCD%% : 兒童導向內容通報標記巨集
* [%URI_ENCODE:variable%] : URI 逸出巨集

> 新視窗巨集中的目標可展開成某個值，而這個值會對應至針對發佈商指定的目標視窗，以及廣告放送位置的廣告版位：

> 如果目標視窗是 _blank，巨集會展開成 1。

> 如果目標視窗是任何其他值，或是未指定任何視窗，巨集將展開成 0。


> 跳脫字元 : & ?


## 參考資料
* [DFP 巨集 - DFP Small Business說明](https://support.google.com/dfp_sb/answer/2376981?hl=zh-Hant)