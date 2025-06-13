# OpenFoam ▽
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


