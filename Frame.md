# 三維側視圖(Iso Surface)
---
1. 視角設定(依照想看的視角而定)

![視角設定](/docs/images/1.將視角設定為XZ方向.png)

2. 顯示畫面中所有的範圍

![顯示畫面](/docs/images/2.顯示畫面中所有的範圍.png)

3. 編輯畫布尺寸

![顯示畫面](/docs/images/9.編輯畫布尺寸.png)

4. 設定畫布尺寸(可依照水槽長與高的比值設定)

![顯示畫面](/docs/images/10.設定畫布尺寸(可依照水槽長與高的比值設定).png)

5. 勾選contour

![顯示畫面](/docs/images/3.勾選contour.png)

6. contour選density

![顯示畫面](/docs/images/4.contour選density.png)

7. 選擇需要的colorbar

![顯示畫面](/docs/images/5.選擇需要的colorBar.png)

8. 刪除低於997.5之密度值(與第10步驟設置相同的密度門檻值，依照案例有所不同)

![顯示畫面](/docs/images/6.刪除低於997.5之密度值.png)

9. 開啟IsoSurface

![顯示畫面](/docs/images/7.開啟IsoSurface.png)

10. 定義密度門檻值(與第8步驟中刪除的密度值相同)

![顯示畫面](/docs/images/8.定義密度門檻值(需與4相同).png)

11. 在contour欄位中只選擇側牆與障礙物的面並關閉障礙物的Contour(這裡的面是在Fluent中的Mesh設定)

![顯示畫面](/docs/images/11.在contour欄位中只選擇側牆與障礙物的面並關閉障礙物的Contour(這裡的面是在Fluent中的Mesh設定).png)

12. 在Shade中將側牆的Shade關閉只保留障礙物的部分，並可以用右鍵點選Shade Color選擇障礙物的顏色

![顯示畫面](/docs/images/12.png)

13. 將Translucency打開可以調整牆的透明度

![顯示畫面](/docs/images/13.將Translucency打開可以調整牆的透明度.png)

14. 可在Zone Style中的Surface Translucency調整牆面透明程度

![顯示畫面](/docs/images/14.可在Zone-Style中的Surface-Translucency調整牆面透明程度.png)

15. 設定完成後可以將Frame儲存起來，後續可以使用Load frame style匯入就不需要每次都要設定(但是!!第10步驟中設定的畫布尺寸還需要自己手動調整)

![顯示畫面](/docs/images/15.png)

# 水槽中心線側視圖
---
- 重複「三維側視圖(Iso Surface)」中1~7步驟
8. 
