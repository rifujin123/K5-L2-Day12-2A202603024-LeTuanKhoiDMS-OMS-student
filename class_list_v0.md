# Danh sách lớp v0 — Lê Tuấn Khôi · G02

## DMS

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng DMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | person | box; seat = driver | Xác định vị trí tài xế | Có, nếu đủ sáng và không bị che |
| 2 | face | box | Xác định vùng mặt để phân tích | Có, tùy góc mặt và che khuất |
| 3 | eye_left / eye_right | open / closed / unknown | Theo dõi trạng thái mắt để hỗ trợ phát hiện buồn ngủ | Có thể; kính hoặc phản xạ có thể che mắt |
| 4 | glasses | none / clear / sun / unknown | Nhận biết kính ảnh hưởng đến quan sát mắt | Có thể; khó phân biệt một số loại kính trên IR |
| 5 | gaze_zone | road / mirror_l / mirror_r / mirror_c / cluster / center / lap / other | Xác định vùng nhìn để hỗ trợ phát hiện mất tập trung | Có thể; phụ thuộc độ rõ mắt và đầu |
| 6 | hand / on_wheel | yes / no / unknown | Nhận biết tay có chạm vô lăng | Có thể; bị giới hạn bởi góc camera và che khuất |
| 7 | phone / state | held / mounted / lap | Nhận biết điện thoại và cách đặt hoặc cầm | Có thể; cần thấy hình dạng điện thoại |
| 8 | face13 | 13 điểm; cờ occluded / outside | Xác định đặc điểm mặt phục vụ phân tích khuôn mặt | Có thể; điểm bị che cần đánh cờ |

## OMS

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng OMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | person / seat | driver / front_passenger / rear_left / rear_middle / rear_right | Xác định người và vị trí trong xe | Có thể, tùy che khuất |
| 2 | person / seatbelt | worn_correct / worn_incorrect / not_worn / unknown | Kiểm tra trạng thái dây an toàn | Có thể; dây tối hoặc bị che thì unknown |
| 3 | face | box | Xác định mặt người ngồi trong cabin | Có thể, nếu thấy mặt |
| 4 | child_seat / occupied | no / unknown | Nhận biết ghế trẻ em và tình trạng quan sát được | Có thể, dựa vào hình dạng |
| 5 | infant_seat / facing | rear / front | Nhận biết nôi và hướng nôi trong xe | Có thể, nếu thấy đủ đặc điểm hướng |
| 6 | object / type | bag / box / cup / other | Nhận biết đồ vật trên ghế | Có thể, dựa vào hình dạng; không đoán màu |
| 7 | seat | driver / front_passenger / rear_left / rear_middle / rear_right | Gắn người hoặc vật với vị trí ghế theo xe | Có thể suy từ vị trí và góc camera |

## 2 câu hỏi leo thang

1. Guideline chưa định nghĩa rõ `infant_seat.facing = rear` và `front` theo hướng nào; khi nôi bị che thì xác định ra sao?
   - Khung ví dụ: S02.
   - Tạm gán: `facing = rear`; cần coach xác nhận cách xác định hướng. `infant_seat` không có thuộc tính `occupied`.
2. Nếu thấy trẻ trong `infant_seat`, cần gán nhãn thế nào khi `infant_seat` không có thuộc tính `occupied` như `child_seat`?
   - Khung ví dụ: S02.
   - Tạm gán: `infant_seat`, `facing = rear`; chưa có thuộc tính để ghi có trẻ, cần hỏi coach xác nhận.
