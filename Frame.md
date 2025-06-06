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

# 水槽中心線側視圖
---
- 重複「三維側視圖(Iso Surface)」中1~7步驟

2-8. 打開切頁功能

![顯示畫面](/docs/images/2-6.打開切頁功能.png)

2-9. 選擇Y-Planes後調整切頁位置

![顯示畫面](/docs/images/2-7.選擇Y-Planes後調整切頁位置.png)

2-10. 利用Extract Slices Over Time 這個功能可以實際的切出一個獨立的面(會在Zone Style中顯示)

![顯示畫面](/docs/images/2-8.png)

2-11. 將圖案轉為2D的呈現方式

![顯示畫面](/docs/images/2-9.將圖案轉為2D的呈現方式.png)

2-12. 輸入想要計算的公式

![顯示畫面](/docs/images/2-10.輸入想要計算的公式.png)

2-13. 將座標和密度無因次化(在首次計算時可以將公式利用Save Equations進行儲存，接著在後續的使用上可以直接將公式Load近來)

![顯示畫面](/docs/images/2-11.png)

2-14. 指定2D座標軸

![顯示畫面](/docs/images/2-12.指定2D座標軸.png)

2-15. 將座標軸指定為無因次化後的座標

![顯示畫面](/docs/images/2-13.將座標軸指定為無因次化後的座標.png)

2-16. 只保留障礙物和切頁，並將障礙物的Contour關閉

![顯示畫面](/docs/images/2-14.只保留障礙物和切頁並將障礙物的Contour關閉.png)

2-17. 點選座標名稱可調整座標的字體等等

![顯示畫面](/docs/images/2-15.點選座標軸可調整座標的字體等等.png)

2-18. 可在此頁面中進行調整

![顯示畫面](/docs/images/2-16.可在此頁面中進行調整.png)

2-19. 調整colorbar

![顯示畫面](/docs/images/2-16-1.調整colorbar.png)

2-20. 可調整colorbar的字體和位置等等

![顯示畫面](/docs/images/2-16-2.可調整colorbar的字體和位置等等.png)

2-21. 同樣可以藉由Save跟Load的功能節省繪圖時間(如果你在TecPlot中進行了額外的操作，如切頁跟無因次化，就必須先完成後才能匯入同樣的frame)

![顯示畫面](/docs/images/2-17.png)
