## sass 快速檔案架構
資料夾結構  
```
|- src
    |- img
    |- sass
        |- base : css reset、typography
        |- component : button、link...
        |- layout : 通用版面，header 、 navgation、footer
        |- pages : 個別頁
        |- utils : variable、mixin、extend 等等
        |- vendors : 放 sass-plugin
        |- section (目前沒有) :  頁面區塊，hero、cta
    - app.sass
    - index.html
```
每個資料夾都有 all.sass 整合資料夾內的 @import 
- base 
    裡面已有 meyer 版本的 reset.css
- utils/mixin
  1. media query breakpoint  
  2. img-url background-image 快速匯入  
    參數 `(<檔案名>,<副檔名>,<複合路徑>(optional))`  
    裡面的 `$root` 可以更換圖片根目錄路徑  
  3. prefix 手動添加瀏覽器前綴  
    參數 `(<css-property>,<value>,<prefix list>)`  
  4. 基礎形狀圓形、三角形  
    圓形參數 `(<size>,<color>)`  
    三角形參數 `(<size>,<三角形位置>,<color>,<預設 1 是等腰，86.6% 為正三角>)`  