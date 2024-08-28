## 1: Tiến hành phân tích về cấu trúc và tiền xử lý các bộ dataset.
a.	Bộ dữ liệu Annual_Surface_Temperature_Change
-	Bộ dữ liệu gồm 72 cột thuộc tính về sự thay đổi nhiệt độ bề mặt hàng năm từ năm 1961 đến 2022. Thay các giá trị null của nhiệt độ từng nằm bằng số 0, trừ cột ISO2 (Internaltional Standard Organization) vì bộ dữ liệu có 225 dòng nên bỏ đi hết các dòng giá trị null sẽ không còn ý nghĩa phân tích.
b.	Bộ dữ liệu Change_in_Mean_Sea_Levels
-	Bộ dữ liệu miêu tả sự thay đổi trung bình của các mực nước biển
-	Cột ‘Date’ có dạng ‘D12/17/1992’ nên cần bỏ chữ D trên đầu.
-	Các giá trị null có giá trị ở cột ‘ISO2’ (tên tiêu chuẩn quốc tế) nên không cần thay thế hay xóa bỏ.
-	Chuyển đổi các kiểu dữ liệu sao cho phù hợp.
c.	Bộ dữ liệu Climate_related_Disasters_Frequency
-	Bộ dữ liệu về tần suất xuất hiện thiên tai, được xử lí bằng cách chuyển về đúng kiểu dữ liệu và điền các giá trị khuyết
d.	Bộ dữ liệu Forest and Carbon
-	Bộ dữ liệu về diện tích rừng và nồng độ Carbon trên khắp thế giới.
## 2: Thu thập số liệu của nhiệt độ, nồng độ CO2, diện tích rừng, và tần suất thiên tai theo quốc gia.
-	Bốn bộ dữ liệu được tách lấy các thông tin cần thiết như đề yêu cầu trong file code
## 3: Tiến hành phân tích sự ảnh hưởng của diện tích rừng lên nhiệt độ, nồng độ CO2, và tuần suất thiên tai theo các khu vực Đông Á và Đông Nam Á.
-	Theo quan sát các bộ dữ liệu ta có:
    •	Dữ liệu nhiệt độ được ghi từ năm 1961 - 2022
    •	Dữ liệu diện tích rừng được ghi từ năm 1992 - 2020
    •	Dữ liệu Carbon được ghi từ năm 1992 - 2020
    •	Dữ liệu về thiên tai được ghi lại từ năm 1980 – 2022
	Để so sánh sự ảnh hưởng thì lấy giai đoạn từ năm 1992 – 2020
Ở Đông Á
    •	Nhiệt độ giữa các năm tăng giảm khác nhau. Nhưng nhìn chung, đến năm 2020 nhiệt độ đã tăng hơn rất nhiều so với năm 1992.
    •	Tầng suất xuất hiện thiên tai của các nước Đông á tăng đỉnh điểm vào khoảng 2012-2016 rồi giảm chạm đáy đến năm 2020.
    •	Từ 1992 - 2020, diện tích rừng và khí thải CO2 đều tăng. Rõ ràng, diện tích rừng càng lớn thì khí thải CO2 sẽ giảm đi nhưng ngược lại là vì do trong khoảng thời gian này các nước Đông Á tập trung phát triển kinh tế nên khí thải CO2 từ công nghiệp tăng lên.

-	Phân tích tương quan Pearson, đánh giá sự tương quan giữa các thuộc tính nhiệt độ, carbon dioxide, tần suất thiên tai với diện tích rừng ở Đông Á:
    •	Mức độ tương quan giữa nhiệt độ và diện tích rừng:  0.6101622703121097
    •	Mức độ tương quan giữa Carbon dioxide và diện tích rừng:  0.9884715509786246
    •	Mức độ tương quan giữa tần suất thiên tai và diện tích rừng:  0.4302178330140335
Khu vực Đông Nam á
-	Nhiệt độ, diện tích rừng, khí CO2, thiên tai đều có xu hướng tăng.
-	So với các nước Đông Á, thì xu hướng các yếu tố khá giống nhưng chỉ khác về thiên tai của các nước Đông Nam Á có xu hướng tăng.
-	Phân tích sự tương quan: 
    •	Mức độ tương quan giữa nhiệt độ và diện tích rừng:  -0.3121822396232287
    •	Mức độ tương quan giữa Carbon dioxide và diện tích rừng:  -0.5308230003803437
    •	Mức độ tương quan giữa tần suất thiên tai và diện tích rừng:  0.3497080476522786
## 4. Tiến hành phân tích tính chất của khí hậu của hai khu vực: Đông Á và Đông Nam Á.
 ![image](https://github.com/user-attachments/assets/6f3fe976-837f-44b9-b8de-0a9e8c5536f0)

-	Nhiệt độ ở các nước Đông Á có khoảng nhiệt độ rộng hơn các nước Đông Nam Á. Tuy nhiên, cần kiểm định có sự khác biệt quá lớn về nhiệt độ của hai khu vực hay không?
-	ANOVA Result for Temperature:
F-statistic: 0.3350454892624368
p-value: 0.5637702435216893
Ta thấy p-value > 0.05 => không có sự khác biệt quá lớn giữa nhiệt độ của hai khu vực: Đông Á và Đông Nam Á.
## 5. Tiến hành phân tích ảnh hưởng của diện tích rừng lên nhiệt độ, nồng độ CO2 và tần suất xuất hiện thiên tai ở Việt Nam.
Tại Việt Nam:
-	Mức độ tương quan giữa nhiệt độ và diện tích rừng:  0.6175697608017235
-	Mức độ tương quan giữa Carbon dioxide và diện tích rừng:  0.8464614152181905
-	Mức độ tương quan giữa tần suất thiên tai và diện tích rừng:  0.4629367283147258

