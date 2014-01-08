CacheControlWithoutMaxAgeTest
=============================

本專案用來測試當 HTTP/1.1 Cache-Control 標頭沒有指定 max-age 參數時，瀏覽器是否會讀取 HTTP/1.0 Expires 標頭指定的到期時間。

* 測試網頁: [http://cache-control.azurewebsites.net/c1.aspx](http://cache-control.azurewebsites.net/c1.aspx)

相關討論
--------------
* [請問使用 Cache-Control: private 標頭，但沒有指定 max-age 快取時間的話，這樣是會快取多久？](http://www.plurk.com/p/irpegu)
