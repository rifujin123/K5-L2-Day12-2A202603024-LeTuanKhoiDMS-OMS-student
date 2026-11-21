# Tự đánh giá — Lê Tuấn Khôi · G02

## 1. Tự rà soát 4 cảnh

Đã kiểm tra độ sát của box và đối chiếu nhãn với guideline. Phát hiện ở đối tượng người lái có mắt bị che nhưng gán `open`; cần đánh giá riêng trạng thái mắt và dùng `unknown` khi không phân biệt được.

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| S02 | Các đối tượng trong ảnh | ok | Kiểm tra box và guideline; không thấy lỗi | Không cần sửa |
| S03 | Các đối tượng trong ảnh | ok | Kiểm tra box và guideline; không thấy lỗi | Không cần sửa |
| D01 | Người lái / mắt | guess | Mắt bị che nhưng gán open; đã sửa thành unknown | Có |
| D04 | Các đối tượng trong ảnh | ok | Kiểm tra box và guideline; không thấy lỗi | Không cần sửa |

## 2. Lỗi mình lặp lại nhiều nhất hôm nay

- Lỗi: nhầm trái và phải.
- Vì sao: đọc guideline chưa kỹ.
- Lần sau: đọc kỹ guideline hơn trước khi gán.

## 3. Ghi chú về disagreement_log

Qua review chéo, mình học cách tăng độ khớp giữa hai annotator, nhận ra và sửa lỗi của mình, đồng thời góp ý để bạn sửa.
