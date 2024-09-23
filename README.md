# Single Image Haze Removal Using Light and Dark Channel Prior
![比較圖 (forest)](https://github.com/user-attachments/assets/2b5d2875-b88b-4b91-8914-fb6a3621d142)<br>
![比較圖 (cones)](https://github.com/user-attachments/assets/89670a38-3b24-420d-b807-04bf785684e6)<br>
![比較圖 (train)](https://github.com/user-attachments/assets/dcf3ba4b-cce0-41be-af0f-fa2419483246)<br>
![比較圖 (buildings)](https://github.com/user-attachments/assets/a916c2b9-bc62-44bb-863f-1ab3a9bae3f3)<br>



Reference : XU, Yueshu, et al. Single image haze removal using light and dark channel prior. In: 2016 IEEE/CIC International Conference on Communications in China (ICCC). IEEE, 2016. p. 1-6.<br><br>
亮、暗通道設計A(X)，改進後的DCP 圖像去霧文章復現<br>
使用python<br><br>
- 原文PDF &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;：[點擊此連結](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7128396)
- 原文DOI &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;：[點擊此連結](https://doi.org/10.1109/TIP.2015.2446191)
- 原作者code &nbsp;：[點擊此連結](https://github.com/JiamingMai/Color-Attenuation-Prior-Dehazing)<br><br>


操作說明 
---
把圖片放進 `my dataset` 資料夾，打開 `my_CAP_main.py` 檔案執行即可<br>
結果圖將儲存在 `my result` 資料夾中。<br><br>


result檔案名稱說明
---
- 原圖名稱
- d &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; : 深度圖
- local_min_d &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; : 深度圖取local_min
- GF_d &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; : 取 guide filter(引導圖=原圖, 輸入圖=local_min_d, r=15, eps=1e-3)
- t &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; : GF_d 還原的 transmission, &beta; = 1
- clip_t &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; : 截斷(t, 0.1, 0.9)
- my_CAP beta=1.0 &nbsp; : 最終去霧結果圖<br><br>

---
關於
---

- 聯繫 : jayabc321@gmail.com
- 復現 : 蕭晉杰
- 時間 : 2024.08.27
