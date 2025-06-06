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

2-9. 利用Extract Slices Over Time 這個功能可以實際的切出一個獨立的面(會在Zone Style中顯示)

![顯示畫面](/docs/images/2-8.利用Extract Slices Over Time 這個功能可以實際的切出一個獨立的面(會在Zone Style中顯示).png)
