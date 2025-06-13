# **OpenFoam ▽**
## 常用指令

| 指令         | 說明                                                                 |
|--------------|----------------------------------------------------------------------|
| `blockMesh`  | 建立計算網格，根據 `system/blockMeshDict` 中的設定生成網格。            |
| `snappyHexMesh` | 以背景網格（通常由 `blockMesh` 產生）為基礎，進行局部細化與幾何擷取。     |
| `setFields`  | 設定初始場，例如指定一區域為特定相（多相流）或速度場等。                   |
| `decomposePar` | 將案例分解為多個處理器子域，以進行平行計算。                           |
| `reconstructPar` | 將平行計算後的結果重組為單一資料夾，方便後處理。                     |
| `mpirun -np <N> <solver> -parallel`   | 啟動平行運算（MPI），將案例在 N 個處理器上運行。需先使用 `decomposePar`。|
| `paraFoam`   | 啟動 ParaView 後處理工具，用於視覺化模擬結果。                          |
| `foamToVTK`  | 將模擬結果轉換為 VTK 格式，方便使用 VTK 或 ParaView 分析。                |
| `checkMesh`  | 檢查網格品質與完整性，是執行模擬前的重要步驟之一。                        |

## 常用修改項目

### 📁 0/ 目錄：初始與邊界條件

| 檔案名稱（依物理場不同） | 常更改項目      | 用意說明                                                   |
|--------------------------|-----------------|------------------------------------------------------------|
| `U`（速度場）            | `internalField` | 設定流場的初始速度值                                        |
|                          | `boundaryField` | 設定各邊界（如 inlet, outlet, wall）的速度條件（固定值、零梯度等） |
| `p`（壓力場）            | 同上            | 設定壓力場的初始值與邊界條件                                |
| 其他如 `alpha.sldge` 等  | 同上            | 多相流模擬中的相分率場設定                                  |

---

### 📁 constant/ 目錄：物理模型與網格參數

| 檔案名稱           | 常更改項目         | 用意說明                                                     |
|--------------------|--------------------|--------------------------------------------------------------|
| `transportProperties` | `nu` 或 `mu`, `rho` | 指定流體的黏滯係數、密度等物性參數                           |
| `LESProperties` | `model`          | 指定實際使用的湍流模型        |
| `polyMesh/blockMeshDict` | 幾何定義區塊         | 設定整體計算域幾何與分格細節                                 |

---

### 📁 system/ 目錄：數值控制與幾何網格設定

| 檔案名稱         | 常更改項目           | 用意說明                                                   |
|------------------|----------------------|------------------------------------------------------------|
| `controlDict`    | `startTime`, `endTime`, `deltaT` | 控制模擬起始時間、結束時間與時間步長                   |
|                  | `writeInterval`       | 設定輸出結果的頻率                                        |
|                  | `application`         | 指定使用的求解器                                          |
| `blockMeshDict`  | `vertices`, `blocks`, `edges`, `boundary` | 幾何與結構網格的設定                             |
| `fvSchemes`      | `divSchemes`, `gradSchemes` 等 | 數值離散方法的選擇                                       |
| `fvSolution`     | `solvers`             | 各物理量的線性求解器設定                                  |
|                  | `SIMPLE`, `PISO`, `PIMPLE` 區塊 | 控制壓力-速度耦合演算法設定                              |
| `decomposeParDict` | `numberOfSubdomains`, `method` | 平行計算設定，如子域數量與分割方式                      |

## 常用邊界條件
###  常見邊界條件設定：壓力場 (p) 與速度場 (U)

| 邊界類型   | 用途 / 物理意義     | 速度 U 設定                         | 壓力 p 設定                         |
|------------|----------------------|--------------------------------------|--------------------------------------|
| `inlet`    | 入口邊界              | `fixedValue`（指定流速）            | `zeroGradient`（允許壓力調整）      |
| `outlet`   | 出口邊界              | `zeroGradient`（允許速度自由出流）  | `fixedValue` 或 `totalPressure`      |
| `wall`     | 固定壁面（無滑移）    | `noSlip`（對應 `fixedValue (0 0 0)`） | `zeroGradient`（壓力隨場調整）       |
| `wall`     | 滑移壁面  | `slip`（允許沿切向滑移）            | `zeroGradient`                       |
| `symmetry` | 對稱面                | `symmetryPlane`                     | `symmetryPlane`                      |
| `empty`    | 2D 模擬中非計算方向   | `empty`                             | `empty`                              |
| `patch`    | 一般定義邊界（需自訂）| 視情況選擇，通常為 `fixedValue` 或 `zeroGradient` | 同左                                  |

---

###  常見邊界條件型別對應說明

| 邊界條件型別      | 用途說明                                                             |
|-------------------|----------------------------------------------------------------------|
| `fixedValue`      | 指定一個固定值（例如入口速度、固定壓力）                             |
| `zeroGradient`    | 對應自然導流或允許變化（例如出口壓力、壁面壓力）                     |
| `noSlip`          | 相當於 `fixedValue (0 0 0)`，壁面上速度為 0                           |
| `slip`            | 無剪切力的滑移壁面，速度可沿切向自由流動                            |
| `symmetryPlane`   | 用於對稱邊界，適用於所有物理量                                       |
| `empty`           | 適用於 2D 模擬中的非作用方向（通常是 z 方向）                        |
| `inletOutlet`     | 可根據流向自動調整是入口還是出口（混合型），常見於自由邊界處        |
| `pressureInletOutletVelocity` | 根據壓力條件決定速度邊界，自由入流或出流（常用於自然對流） |





