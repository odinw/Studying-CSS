

# 如何撰寫css
- 展示在 div 寫 css 屬性, 讓這個區塊的內容都套用
- css 內外層重複時, 以內層為主
- style 告知樣式
  - color 顏色, ex: red
  - font-size 字體大小, ex: 20px
  - background-color 背景顏色, ex: blueviolet
  - border 設定邊框
    - px 值, 邊框厚度
    - solid 實線, dashed 虛線
    - width 寬度, height 高度
    - max-width 自動縮放的最大寬度
      - 當畫面寬度 小於 最大寬度, 則寬度會縮放為畫面最大寬度
      - 當畫面寬度 大於 最大寬度, 則寬度為 max-width
    - max-height 自動縮放的最大高度, 邏輯相同
- [如何撰寫css](https://youtu.be/sDUWDtrvizI?si=vy7aUsZNfgUOL7rC)

# color 顏色
- color
  - 字串表示, ex: red
  - 數字編碼表示法, ex: #AABB55
  - rgb 表示法, ex: rgb(200, 30, 180)
  - hsl 表示法, ex: hsl(20, 60%, 50%)
- background-color 背景色, 用法比照 color
- [color 顏色](https://youtu.be/OjPzTq-NJw0)

# padding & margin
- 都是用來控制空間
- margin 控制外部空間
- padding 控制內部空間
  - 只管單邊間隔, 就加上 -top, -bottom, -left, -right
  - 指定數值 單一 px, 表示內部四周都用相同的間隔
  - 指定數值 四個 px, 表示內部四周分別指定間隔
  - 指定數值 可以是負數, 用此能重疊到其他物件的空間
- [padding & margin](https://youtu.be/xmsh58bBSbc)

# float & display
- float 讓原本佔位整列的標籤浮起來 (ex: img), 讓後續標籤可靠近, 並列排版, 可用於: 需圖文並茂的時機, 網頁列表與網頁內容並茂的時機
- display 可調整標籤的空間佔位模式, 把預設佔一整列的改為 用多少佔多少, 也可反之操作
- [float & display](https://youtu.be/GSVNg5CzVnw)

# [position 定位](https://youtu.be/k4s6ynrkw6A)
- fixed 固定
  - 已整個畫面為視角的左上為原點 在定位?
- relative 相對定位
  - 已當前位置為原點, 再做偏移
- absolute 絕對定位

# [opacity & border-radius](https://youtu.be/3sA7bZ5jx2E)
- opacity 透明度
  - 值域: 0% ~ 100%, 0% 完全透明, 100% 完全不透明
- border-radius 圓邊
  - 設定單值小於半徑, 是圓角效果
  - 設定單值等於半徑 (此為最大值), 若原本是正方形 就會變正圓
  - 分別設定 4 個角, 給 4個值 意義分別是設定(順時鐘): 左上 > 右上 > 右下 > 左下

  # [style標籤](https://youtu.be/J67_ev6VdJA)
  CSS 的寫法
  1. 直接寫在 tag 中, 就如同之前的範例
  2. 把 css 從 標籤中抽離到 head 的 style, 就能大範圍套用 (本次作法)

  # [引入外部css檔案](https://youtu.be/AlqMknuXSFc)
  - 獨立建立 .css
  - 再到 .html head 區塊, 用 link 標籤將 .css 引入
  - 依此方式, 
  - 優點
   - 責任分離：獨立 .css，讓腳本責任明確，css 負責風格、html 負責排版
   - 重用性：同份 .css 就能給多個 html 使用, 不用重複寫
   - 一致性：修改也能一起改, 適合規格上必定相同風格
  - link
    - rel 說明檔案類型
    - href 檔案路徑

# [class & id](https://youtu.be/bgiPH9GXmJ4)
- 是用來對 標籤 進行分類(class) 或 唯一標記(id), 以利精準的套用 css 可以風格對象
- id 則是具有唯一性的標記, 在單份 .html 不會出現使用相同 id 的標籤。
- class 適合有相同狀況的群組類型標籤, 因此相同 class 可套用到多個標籤上
- 同個 標籤 可以放上多個 class
所以適合用在單獨類型的對象
- 如何在 .css 中標記
  - .{class_name} 為 class
  - #{id_name} 為 id

# [selector](https://youtu.be/tvQEdXx-_cY)
css selector 有許多指定方式
- html
  - tag 單一標籤, ex: p, input
  - nested tags 巢狀標籤, 第一個標籤為目標容器, 第二標籤為容器底下的目標
    - ex: dl dd, 目標是 dl 結構下的 dd。所以 若 dl 底下有 dt 則不受影響
  - : 以冒號指定行為
    - ex: h3:hover
- 自訂
  - class: .{class_name} 點號開頭
  - id: #{id}
- 多重混用
  - ex: #id-1 .class-1 {...}
- * 單個米字號 表示全套用, 但似乎順序性較低? 實測若有其他樣式指定了同屬性 則以其他樣式優先
- 針對屬性 [], 此為跨越標籤的設定, 只要有標籤帶有此屬性 就會套用
  - ex: type
- 行為
  - {其他selector指定模式} 加上冒號 : 加上 {行為}
  - ex: h3:hover, 此為 {tag}:{行為}
- ※ 這裡只展示常用的，但還有很多方式可查看 W3C 