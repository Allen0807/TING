# ANSYS Fluent 17.2
---
## 模型幾何繪製
---
- 擠出功能(Extude)
- Operation

  Add Material：增建模型
  
  Cut Material：將增建出之模型減去
  
  Slice Material：將增建之模型截成數塊

- 陣列功能(Create→Pattem)
- Pattem Type

  Linear：單方向陣列
  
  Rectangular：包含橫向及縱向陣列

## 模型網格設置
---
- 自動建立網格
- 手動建立網格
- 網格數及品質查看
  
  Mesh→Statistics→Mesh Metri→Element Quality

 >當數值愈接近1時，代表網格形狀較為均勻。

## 模型運算設定
---
### 紊流模式設定
- 混合模式設定

![動態Cs](/docs/images/Mulyiphase-Model.jpg)

- 動態Cs參數

![動態Cs](/docs/images/Viscous-Model.jpg)

- 靜態Cs參數

![靜態Cs](/docs/images/Viscous-Model-Cs.jpg)

>目前我們是用動態，但ANSYS版本無法直接輸出Cs值，靜態比較保險(需與老師討論)
