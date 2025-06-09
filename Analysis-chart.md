# 分析工具
---
## Affter Effects
---
- 剪裁與輸出

## Grapher
- 輸入資料

  將資料複製到Worksheet Manager表格中

- 繪製曲線

  Home→Basic→Line Plot

- Plot

  Data：選取對應x、y軸資料

  Add to Graph：複製一條線 (x軸不變、y軸下一行)

- Symbol

  Frequency：幾筆資料呈現一個符號

  Symbol：選取符號樣式

  Fill：符號內部樣式設定

  Line：符號外框樣式設定

- Line：設定線段樣式

> 通常Symbol跟Line會擇一，不然會太亂。

- Error Bars

  Drection：Vertical

  Type：Read of data variable

  variable：設定差值

  Vertical direction：Positive (線上方) or Negative (線下方)

  - 調整軸座標 (X Axis、YAxis)
- Axis

  Limits:調整最大最小值

  Title→Title Properties→Text：輸入軸座標名稱

- Ticks

  Maijor Ticks：調整大尺度座標設置 (有數字的)

  Miner Ticks：調整小尺度座標設置 (大尺度間沒數字的)

- Labels

  Label Settings→Label Format

  Font：調整字型、大小

  Format：調整小數點

- 圖例設置 (Legend)
- 新增圖例：圖面上典右鍵→Add Legend
- Title→Title Properties→Text：輸入軸圖例名稱
- Entries

  All Entries：選擇域呈現出資訊

  Individual Entries：重新編譯資料名稱、順序
  

## Matlab
---
- 計算Ansys輸出文字檔
> 確認各資料欄位對應正確

### 俊廷

| 分析項目         | 檔名       | 輸出副檔名 |
|--------------|---------------|------|
| 頭端速度分析  | Current_head.mlx | .dat |
| 質量通量及動量通量 | Momentum and Mass flux.mlx | .dat |
| HovmOller     | Hovmoller.mlx | .dat |
| 動能及位能     | EUV.mlx | .dat |
| Z方向動能     | Energy in Zdiretion.mlx | .dat |
| 背景位能演化     | Diffusion.m | .dat |
| 重流體分區     | Diffusion2.m | .dat |
| 背景位能暫態     | DiffusionXZ.m | .dat |
| 動態背景位能     | dynamic-mixing-rate.mlx | .dat |
| 時均UV諾應力     | Reynolds_stress.mlx | .dat |
| 時均TKE解析 | TKE.mlx | .dat |
| 空間平均TKE解析 (俯視圖) | TKEtop.mlx | .dat |
| 空間平均TKE解析 (側視圖) | TKEside.mlx | .dat |
| AVI 轉 GIF| AVI TO  GIF.mlx | .gif |
| IMAGE 轉 GIF| IMAGE TO  GIF.mlx | .gif |
| 以色皆抓取頭端資料 | RGB | - |
| 以色皆抓取頭端資料(模擬上俯視 ISO = 997.5) | IMAGE TO  GIF.mlx | - |

### 敬原

| 指標 | 程式碼 | 輸出格式 |
|------|----------|----------|
| 密度、速度、壓力場的切面資料 | `Density_Presure_Velocity_Slice.m` | .dat  |
|  密度資料(最大範圍)| `Flow_extent.m`| .dat |
|  密度高程資料| `Elevation_max.m`| .dat |
|  質量通量, 動量通量| `Flux.m`| .jpg |
|  密度等值線之堆疊| `Lobe_and_Cleft_Velocity.m`| .dat |
|  主支流重流體體積(質量)| `mass_consevation.m`| .dat |
|  紊流動能解析度| `TKE_vaildation.m`| .dat |

## Tecplot
---
### 匯入圖檔
### 3D功能列
#### 網格 (Mesh)
  
- 配合Zone Style可勾選欲呈現之網格設置，並調整線粗及顏色。

> 目前用於論文中網格配置示意圖呈現。

![網格功能](/docs/images/Mesh.jpg)

#### 顏色及資料 (Contour) (常用)
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

#### 面 (Shade)
  
  將網格設定時所取名的面顯示出來
   
#### 向量 (Vector)
  
  呈現出向量符號
  
#### 邊 (Edge)
  
  繪製截面時義於呈現
  
#### 資料點 (Scatter)
  
  再資料較少時可顯示出來
  
#### Zone Style (常用)
  
  調整各個前述功能於面上的呈現
  
#### 等值表面 (Iso-surfaces)
  
  繪製流體等值面
  
#### 切頁 (Slices)
  
  單時刻切頁
  全時刻切頁
  
#### 打光 (Lighting)
  
  可調整打光方位(通常適用於3D成現，2D會關掉)
  
#### 透明度 (Translucency)
  
  調整個面上的透明條件
