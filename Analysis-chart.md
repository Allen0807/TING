# 分析工具
---
## Affter Effects
---
- 剪裁與輸出

## Matlab
---
- 計算Ansys輸出文字檔
- GIG、AVI、JPG轉換

## Tecplot
---
### 匯入圖檔
### 3D功能列
#### 網格(Mesh)
  
- 配合Zone Style可勾選欲呈現之網格設置，並調整線粗及顏色。

![網格功能](/docs/images/Mesh.jpg)

>目前用於論文中網格配置示意圖呈現。

#### 顏色及資料(Contour)(常用)
##### 資料與顏色設置 (Level and Color)  
- 選取與繪製資料 (速度場、密度場...)

![資料選取](/docs/images/Data.jpg)

- 調整Color bar劃分 (Contour levels→Set levels)

  調整Minimum level (最小值)、Maximul (最大值)以及Number of levels (將最大及最小值內切成幾格)

![劃分](/docs/images/Set-levels.jpg)

- 調整Color bar顏色
>常用Small Rainbow、Diverging-Blue/Red、Two Color

![顏色調整](/docs/images/Color-map.jpg)

- 儲存及匯入Color bar
  Rename：重新命名
  Delete：刪除
  Import：匯入
  Export：匯出

![顏色儲存](/docs/images/color-map-save.jpg)

- Color map distribution method

  Banded：採用上面Contour levels的數值進行等值線的分布並上色
  
  Continuous：設定最大及最小值以差分變得連續
  
  Reset to contour variable min/max：以輸入資料之最大及最小值設定數值
  
  Reset to contour level min/max：以Set Levels設定的最大及最小值設定數值
  
>通常以Reset to contour level min/max才能讓圖上的顏色跟Color bar對應。

![顏色連續](/docs/images/Color-map-Continuous.jpg)

- Color cutoff

  Cut above：刪除設定值以上的數值
  
  Cut bolow：刪除設定值以下的數值

- Color map adjustments

  Reverse：反轉Color bar (例如：紅+藍- → 紅-藍+)

#### 面(Shade)
  
  將網格設定時所取名的面顯示出來
   
#### 向量(Vector)
  
  呈現出向量符號
  
#### 邊(Edge)
  
  繪製截面時義於呈現
  
#### 資料點(Scatter)
  
  再資料較少時可顯示出來
  
#### Zone Style(常用)
  
  調整各個前述功能於面上的呈現
  
#### 等值表面(Iso-surfaces)
  
  繪製流體等值面
  
#### 切頁(Slices)
  
  單時刻切頁
  全時刻切頁
  
#### 打光(Lighting)
  
  可調整打光方位(通常適用於3D成現，2D會關掉)
  
#### 透明度(Translucency)
  
  調整個面上的透明條件
