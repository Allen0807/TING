![image](https://github.com/user-attachments/assets/39538086-9fd0-4be3-a28d-a03a6a0cb00a)# ANSYS Fluent 17.2
---
## 模型幾何繪製
---
- 擠出功能 (Extude)
- Operation

  Add Material：增建模型
  
  Cut Material：將增建出之模型減去
  
  Slice Material：將增建之模型截成數塊

- 陣列功能 (Create→Pattem)
- Pattem Type

  Linear：單方向陣列
  
  Rectangular：包含橫向及縱向陣列

- 聯集面功能 (Share Topology)

  將所有的Solid集合成一個Part，接著Generate成一個Share Topology，讓網格再同一面是一樣大的 (資料的傳遞較不易失真)


## 模型網格設置
---
- 自動建立網格
- 手動建立網格

  參考網址 (圓柱均勻網格建置)：https://www.youtube.com/watch?v=0tmMeSQTqRs

- 網格數及品質查看
  
  Mesh→Statistics→Mesh Metri→Element Quality

 >當數值愈接近1時，代表網格形狀較為均勻。

## 模型運算設定
---
### 紊流模式設定 (Models)
- 混合模式設定

![動態Cs](/docs/images/Mulyiphase-Model.jpg)

- 動態Cs參數

![動態Cs](/docs/images/Viscous-Model.jpg)

- 靜態Cs參數

  更改其中Cs值可以控制亞網格模型模擬到的網資料 (通常Cs=0.1~0.3)
  
> 目前我們是用動態，但ANSYS版本無法直接輸出Cs值，靜態比較保險(需與老師討論)

![靜態Cs](/docs/images/Viscous-Model-Cs.jpg)

### 邊界條件設定 (Boundary Conditions)

> 跟老師好好討論再設定 (超重要)

### 演算法與差分設定 (Solution Methods)

- PISO
- Gradient：Least Square Cell Based
- Pressure：PRESTO!
- Momentum、Volume Fraction、Energy：QUICK
- Transient Order Implicit

> Volume Fraction、Energy可以跟老師討論看看

### 收斂條件設定 (Monitors→Residual Monitors)

- continuity：10^-4
- x、y、z-velocity：10^-5
- energy：10^-6
- vf-phase-2：10^-3

> 這可能需要跟老師討論，跟精度有極大關係 (超重要)

### 模擬資料 (Run Calculation)

- Time Step Size：0.002 (依據庫朗數)
- Number of Time Step：8000 (依據總體模擬時長)
- Data Sampling for Time Statistics (輸出額外資料要打勾)
- Max Iterations/Time Step：10000 (最大迭代次數)

> 先跟老師商量好再設定 (超重要)

### 輸出檔設定 (Calculation Activities)

- 圖檔輸出 Autosave Every (Time Step) :100 (乘上Time Step可知道每幾秒輸出一次，通常0.1 or 0.2s)
- 文字檔輸出 Automatic Export：Ceate→Solution Data Export

  File Type：ASCII
  
  Location：Cell center
  
  Delimiter：Comma
  
  Frequency (Time Step)：50 (通常乘上Time Step為0.1s)
  
  Quantities：

| 輸出資料 | 英文名稱|
|--------------|---------------|
| 靜壓 | static-pressure |
| 動壓 | dynamic-pressure |
| 總壓 | total-pressure |
| 密度 | density |
| X速度 | x-velocity |
| Y速度 | y-velocity |
| Z速度 | z-velocity |
| 總能量 | total-energy |
| 內能| internal-energy |
| X擾動速度 | rmse-x-velocity |
| Y擾動速度 | rmse-y-velocity |
| Z擾動速度 | rmse-z-velocity |
| 雷諾應力UV | resolved-uv-stress |
| 雷諾應力UW | resolved-uw-stress |
| 雷諾應力VW | resolved-vw-stress |
| 濾波長度 | sgs-filter-length |
| 亞網格動力黏滯係數 | sgs-dynamic-visc-const |
| 網格體積 | cell-volume |
| 剪應變率 | strain-rate-mag |

> 跟分析有關，跟老師確定一下是否增減

### 指定重流體區域 (Solution Initialization)
- Initialize
- Mark→Region→設定重流體存在座標→Mark
- Patch
