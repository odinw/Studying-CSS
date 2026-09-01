

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