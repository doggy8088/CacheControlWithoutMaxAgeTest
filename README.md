CacheControlWithoutMaxAgeTest
=============================

本專案用來測試當 HTTP/1.1 Cache-Control 標頭沒有指定 max-age 參數時，瀏覽器是否會讀取 HTTP/1.0 Expires 標頭指定的到期時間。

* 測試網頁: [http://cache-control.azurewebsites.net/c1.aspx](http://cache-control.azurewebsites.net/c1.aspx)

    ```aspx
    <%@ Page Language="C#" AutoEventWireup="true" CodeBehind="C1.aspx.cs" Inherits="WebApplication1.C1" %>

    <!DOCTYPE html>

    <html xmlns="http://www.w3.org/1999/xhtml">
    <head runat="server">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
        <title></title>
    </head>
    <body>
        <form id="form1" runat="server">
        <pre>
    Expires: <%=DateTime.Now.AddMinutes(1).ToUniversalTime().ToString("R") %>
    Cache-Control: private
        </pre>
        </form>
    </body>
    </html>
    ```

相關討論
--------------
* [請問使用 Cache-Control: private 標頭，但沒有指定 max-age 快取時間的話，這樣是會快取多久？](http://www.plurk.com/p/irpegu)
