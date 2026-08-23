

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