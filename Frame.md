# 1.三維側視圖(Iso Surface)
---
1-1. 視角設定(依照想看的視角而定)

![視角設定](/docs/images/1.將視角設定為XZ方向.png)

1-2. 顯示畫面中所有的範圍

![顯示畫面](/docs/images/2.顯示畫面中所有的範圍.png)

1-3. 編輯畫布尺寸

![顯示畫面](/docs/images/9.編輯畫布尺寸.png)

1-4. 設定畫布尺寸(可依照水槽長與高的比值設定)

![顯示畫面](/docs/images/10.設定畫布尺寸(可依照水槽長與高的比值設定).png)

1-5. 勾選contour

![顯示畫面](/docs/images/3.勾選contour.png)

1-6. contour選density

![顯示畫面](/docs/images/4.contour選density.png)

1-7. 選擇需要的colorbar

![顯示畫面](/docs/images/5.選擇需要的colorBar.png)

1-8. 刪除低於997.5之密度值(與第10步驟設置相同的密度門檻值，依照案例有所不同)

![顯示畫面](/docs/images/6.刪除低於997.5之密度值.png)

1-9. 開啟IsoSurface

![顯示畫面](/docs/images/7.開啟IsoSurface.png)

1-10. 定義密度門檻值(與第8步驟中刪除的密度值相同)

![顯示畫面](/docs/images/8.定義密度門檻值(需與4相同).png)

1-11. 在contour欄位中只選擇側牆與障礙物的面並關閉障礙物的Contour(這裡的面是在Fluent中的Mesh設定)

![顯示畫面](/docs/images/11.在contour欄位中只選擇側牆與障礙物的面並關閉障礙物的Contour(這裡的面是在Fluent中的Mesh設定).png)

1-12. 在Shade中將側牆的Shade關閉只保留障礙物的部分，並可以用右鍵點選Shade Color選擇障礙物的顏色

![顯示畫面](/docs/images/12.png)

1-13. 將Translucency打開可以調整牆的透明度

![顯示畫面](/docs/images/13.將Translucency打開可以調整牆的透明度.png)

1-14. 可在Zone Style中的Surface Translucency調整牆面透明程度

![顯示畫面](/docs/images/14.可在Zone-Style中的Surface-Translucency調整牆面透明程度.png)

1-15. 設定完成後可以將Frame儲存起來，後續可以使用Load frame style匯入就不需要每次都要設定(但是!!第10步驟中設定的畫布尺寸還需要自己手動調整)

![顯示畫面](/docs/images/15.png)

# 2.水槽中心線側視圖
---
- 重複「三維側視圖(Iso Surface)」中1~7步驟

2-1. 打開切頁功能

![顯示畫面](/docs/images/2-6.打開切頁功能.png)

2-2. 選擇Y-Planes後調整切頁位置

![顯示畫面](/docs/images/2-7.選擇Y-Planes後調整切頁位置.png)

2-3. 利用Extract Slices Over Time 這個功能可以實際的切出一個獨立的面(會在Zone Style中顯示)

![顯示畫面](/docs/images/2-8.png)

2-4. 將圖案轉為2D的呈現方式

![顯示畫面](/docs/images/2-9.將圖案轉為2D的呈現方式.png)

2-5. 輸入想要計算的公式

![顯示畫面](/docs/images/2-10.輸入想要計算的公式.png)

2-6. 將座標和密度無因次化(在首次計算時可以將公式利用Save Equations進行儲存，接著在後續的使用上可以直接將公式Load進來)

![顯示畫面](/docs/images/2-11.png)

2-7. 指定2D座標軸

![顯示畫面](/docs/images/2-12.指定2D座標軸.png)

2-8. 將座標軸指定為無因次化後的座標

![顯示畫面](/docs/images/2-13.將座標軸指定為無因次化後的座標.png)

2-9. 只保留障礙物和切頁，並將障礙物的Contour關閉

![顯示畫面](/docs/images/2-14.只保留障礙物和切頁並將障礙物的Contour關閉.png)

2-10. 點選座標名稱可調整座標的字體等等

![顯示畫面](/docs/images/2-15.點選座標軸可調整座標的字體等等.png)

2-11. 可在此頁面中進行調整

![顯示畫面](/docs/images/2-16.可在此頁面中進行調整.png)

2-12. 調整colorbar

![顯示畫面](/docs/images/2-16-1.調整colorbar.png)

2-13. 可調整colorbar的字體和位置等等

![顯示畫面](/docs/images/2-16-2.可調整colorbar的字體和位置等等.png)

2-14. 同樣可以藉由Save跟Load的功能節省繪圖時間(如果你在TecPlot中進行了額外的操作，如切頁跟無因次化，就必須先完成後才能匯入同樣的frame)

![顯示畫面](/docs/images/2-17.png)

2-15. 新增障礙物的frame

![顯示畫面](/docs/images/2-18.新增障礙物的frame.png)

2-16. 匯入一個圖檔即可

![顯示畫面](/docs/images/2-20.匯入一個圖檔即可.png)

2-17. 進行切頁(2-8 ~ 2-10)和無因次(2-12 ~ 2-13)的操作後利用Load frame style便可以匯入設定好的frame

2-18. 調整畫布大小與位置使其與原先的畫布重合

![顯示畫面](/docs/images/2-19.調整畫布大小與位置使其與原先的畫布重合.png)

2-19. 匯出檔案，Region必須選擇All frames才能匯出兩個frame，寬度方面可以盡量大一點提高解析度，Antialiasing用途為減少畫面的鋸齒可自行調整(2-16)，Encoding為畫面的編碼的方法選擇標準即可，最後品質一定是開到最高

![顯示畫面](/docs/images/2-21-1.匯出檔案.png)

# 3.三維圖及俯視圖(Iso Surface)

- 重複1-1 ~ 1-10的步驟，只需要調整視角即可

3-1. 開啟邊界

![顯示畫面](/docs/images/3-1開啟邊界.png)

3-2. 開啟所有牆面

![顯示畫面](/docs/images/3-2.開啟所有牆面.png)

3-3. 關閉頂部和前方牆面的shade

![顯示畫面](/docs/images/3-3.關閉頂部和前方牆面的shade.png)

3-4. 只保留障礙物的邊界

![顯示畫面](/docs/images/3-4.只保留障礙物的邊界.png)

3-5. 調整邊界透明度

![顯示畫面](/docs/images/3-5.調整邊界透明度.png)

3-6. 儲存frame以利後續使用，最後進行匯出的動作

# 4.通量切頁圖

- 重複「3.三維圖及俯視圖(Iso Surface)」的步驟，或者是直接匯入3-16所儲存的frame

4-1. 在排樁上游處切頁

![顯示畫面](/docs/images/4-1.在排樁上游處切頁.png)

4-2. 利用Extract Slices Over Time 這個功能可以實際的切出一個獨立的面(會在Zone Style中顯示)

![顯示畫面](/docs/images/4-1-1.png)

4-3. 在排樁下游處切頁

![顯示畫面](/docs/images/4-2.在排樁下游處切頁.png)

4-4. 利用Extract Slices Over Time 這個功能可以實際的切出一個獨立的面(會在Zone Style中顯示)

![顯示畫面](/docs/images/4-1-1.png)

4-5. 開啟所有的面

![顯示畫面](/docs/images/4-3.開啟所有的面.png)

4-6. 設定shade

![顯示畫面](/docs/images/4-4.設定shade.png)

4-7. 右鍵點選Edge Color可選擇邊界線條的顏色

![顯示畫面](/docs/images/4-5.png)

4-8. 同樣可調整面的透明度

![顯示畫面](/docs/images/4-6.同樣可調整面的透明度.png)

4-9. 儲存frame以利後續使用，最後進行匯出的動作

# 5.Q Criterion
---
5-1.點選Analyze中的Caculate Variables功能

![視角設定](/docs/images/5-1.png)

5-2.利用select計算不同的變數

![顯示畫面](/docs/images/5-2.利用select計算不同的變數.png)

5-3.選擇Q_Criterion

![顯示畫面](/docs/images/5-3.選擇Q_Criterion.png)

5-4.將計算位置設定在網格中心後便可以計算

![顯示畫面](/docs/images/5-4.將計算位置設定在網格中心後便可以計算.png)

5-5.在contour的details中進行選擇

![顯示畫面](/docs/images/5-5.在contour的details中進行選擇.png)

5-6.選擇想呈現的contour_如Q_Criterion

![顯示畫面](/docs/images/5-6.選擇想呈現的contour_如Q_Criterion.png)

5-7.可選擇欲使用的contour顏色

![顯示畫面](/docs/images/5-7.可選擇欲使用的contour顏色.png)

5-8.開啟IsoSurface後可選擇顯示幾個數值並在Value中定義

![顯示畫面](/docs/images/5-8.開啟IsoSurface後可選擇顯示幾個數值並在Value中定義.png)

5-9.Zone Style中可選擇想要顯示的牆面 

![顯示畫面](/docs/images/5-9.png)

# 6.Vorticity
---
6-1.點選Analyze中的Caculate Variables功能

![視角設定](/docs/images/6-1.png)

6-2.利用select計算不同的變數

![顯示畫面](/docs/images/6-2.利用select計算不同的變數.png)

6-3.選擇Z Vorticity後按OK

![顯示畫面](/docs/images/6-3.png)

6-4.將計算位置設置在網格中心處

![顯示畫面](/docs/images/6-4.將計算位置設置在網格中心處.png)

6-5.利用Slice功能將Z=0的平面進行切頁

![顯示畫面](/docs/images/6-5.利用Slice功能將Z=0的平面進行切頁.png)

6-6.利用Data中Extract的Extract Slices Over Time將每個時間步的檔案都進行切頁的步驟

![顯示畫面](/docs/images/6-6.png)

6-7.進入Data中Alter的Specify Equations功能

![顯示畫面](/docs/images/6-7.png)

6-8.以方柱邊長為特徵長度並搭配特徵速度將渦度進行無因次化

![顯示畫面](/docs/images/6-8.以方柱邊長為特徵長度並搭配特徵速度將渦度進行無因次化.png)

6-9.在Contour中的Details中便可以選擇計算的無因次渦度場

![顯示畫面](/docs/images/6-9.在Contour中的Details中便可以選擇計算的無因次渦度場.png)

6-10.匯入color map(路徑:I/論文圖檔/6模擬圖檔-Vorticity/Vorticity_Qcriterion.map)

![顯示畫面](/docs/images/6-10.png)

6-11.選擇Vorticity的color map

![顯示畫面](/docs/images/6-11.png)

6-12.利用set level設定color bar

![顯示畫面](/docs/images/6-12.png)

6-13.設定最大及最小值和間距

![顯示畫面](/docs/images/6-13.設定最大及最小值和間距.png)

6-14.將contour、shade、edge打開

![顯示畫面](/docs/images/6-14.將contour、shade、edge打開.png)

6-15.在contour欄位中僅保留障礙物和切頁，其中關閉障礙物的contour

![顯示畫面](/docs/images/6-15.在contour欄位中僅保留障礙物和切頁，其中關閉障礙物的contour.png)

6-16.在shade中利用右鍵點選可更換顏色

![顯示畫面](/docs/images/6-16.在shade中利用右鍵點選可更換顏色.png)

6-17.在Edge欄位中僅保留障礙物

![顯示畫面](/docs/images/6-17.在Edge欄位中僅保留障礙物.png)

# 7.向量圖
---
7-1.首先利用切頁功能將切頁位置定為流向中心處

![視角設定](/docs/images/7-1.首先利用切頁功能將切頁位置定為流向中心處.png)

7-2.利用Data中Extract的Extract Slices Over Time將每個時間步的檔案都進行切頁的步驟

![顯示畫面](/docs/images/7-2.png)

7-2-2.將座標和密度無因次化

![顯示畫面](/docs/images/7-3.png)

7-3.開啟contour後在下拉選單中選取Density

![顯示畫面](/docs/images/7-3.開啟contour後在下拉選單中選取Density.png)

7-4.開啟ZoneStyle後將障礙物的contour關閉，並將Density的contour type選擇lines的方式呈現

![顯示畫面](/docs/images/7-4.png)

7-5.可在line color中選擇線的顏色，並在line thinkness改變線的粗細

![顯示畫面](/docs/images/7-5.png)

7-6.將色彩選擇為multi1

![顯示畫面](/docs/images/7-6.將色彩選擇為multi1.png)

7-7.可在shade中關閉切頁使背景為白色

![顯示畫面](/docs/images/7-7.可在shade中關閉切頁使背景為白色.png)

7-8.線條數量可由contour中的set level中設定間距便可改變數量

![顯示畫面](/docs/images/7-8.png)

7-9.將圖像檢視座標設定為2D

![顯示畫面](/docs/images/7-9.將圖像檢視座標設定為2D.png)

7-10.將向量打開

![顯示畫面](/docs/images/7-10.將向量打開.png)

7-11.藉由point中的index skip功能可以改變向量箭頭數量

![顯示畫面](/docs/images/7-11.png)
