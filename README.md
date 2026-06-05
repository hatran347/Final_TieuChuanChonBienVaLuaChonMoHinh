# Chủ đề 4: Lựa chọn mô hình và lựa chọn biến
**Môn học:** Mô hình hóa thống kê  
**Bộ dữ liệu:** Diabetes (package lars) 
**Link reposity:** https://github.com/hatran347/Final_TieuChuanChonBienVaLuaChonMoHinh

## Giới thiệu

Báo cáo trình bày các phương pháp tiêu chuẩn lựa chọn biến và phương pháp lựa chọn mô hình hồi quy tuyến tính, thực nghiệm trên bộ dữ liệu Diabetes. Các mô hình được đánh giá bằng các tiêu chuẩn như R², Adjusted R², Mallows' Cp, AIC, BIC, đồng thời được kiểm định và đánh giá độ ổn định thông qua các kỹ thuật Cross-Validation.

Để chạy toàn bộ các đoạn code trong báo cáo này, cần chuẩn bị các thư viện sau:

install.packages(c( "tidyverse", "leaps", "boot", "lars", "knitr", "kableExtra","scales","corrplot",
"ggplot2", "tidyr"))

## Phân công công việc và mức độ đóng góp

| Thành viên         | Công việc                                                                      | Mức độ hoàn thiện |
| ------------------ | ------------------------------------------------------------------------------ | ----------------- |
| Vũ Hà Thư          | Tiêu chuẩn lựa chọn biến                                                       | 100%              |
| Nguyễn Đình Mai Vi | Lựa chọn mô hình và các kiểm định                                              | 100%              |
| Trần Việt Hà       | Tổng hợp nội dung, code minh họa                                               | 100%              |

## Câu hỏi thảo luận

1. Khi xây dựng mô hình, tại sao người ta lại phải chia dataset ra thành các tập train và test và tại sao tỉ lệ thường sử dụng là 80-20 hoặc 70-30. Vậy trong trường hợp dữ liệu có đến khoảng 10 triệu records thì có nhất thiết phải chia tỉ lệ này hay không.
2. Forward và Backward có vẻ như là đang làm ngược chiều nhau. Giả sử trên cùng 1 tập dataset, áp dụng 2 phương pháp Backward và Forward thì kết quả sẽ như thế nào? Giả sử bộ dữ liệu có 2 biến X1 và X2 tương quan với nhau mạnh, và cả 2 cùng tác động lên Y. Phân tích sai lầm của Forward và Backward có thể mắc phải với cặp biến này?
