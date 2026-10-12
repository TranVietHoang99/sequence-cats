# 🐾 Sequence Mèo

Game **Sequence** chủ đề mèo, chơi online 1 đấu 1 ngay trên trình duyệt, không cần cài đặt hay tài khoản.
Có **10 mèo kỹ năng** và **7 bản đồ** với địa hình.

👉 Chơi tại: https://tranviethoang99.github.io/sequence-cats/

## Cách chơi với bạn bè
1. Mở trang game, nhập tên, bấm **Tạo phòng**.
2. Chọn luật: bản đồ, mèo kỹ năng, số lá trên tay, thời gian mỗi lượt, số sequence để thắng.
3. Gửi **mã phòng** hoặc **link** cho bạn bè; bạn bè nhập tên và bấm **Vào phòng**.
4. Người tạo phòng (chủ phòng) phải **giữ tab mở** suốt ván, vì máy chủ phòng giữ trạng thái ván chơi.
   Chủ phòng có thể đổi luật giữa chừng bằng nút ⚙️ Luật.

## Luật cơ bản
- Chọn 1 lá trên tay, các ô dùng được sẽ sáng lên, bấm vào ô để đặt dấu chân 🐾.
- 5 dấu chân liên tiếp (ngang/dọc/chéo) = 1 sequence. Bát cá ở góc và hộp giấy là ô tự do, tính cho cả hai bên.
  Hai sequence được dùng chung tối đa 1 ô.
- **Mèo Joker** (mèo mở 2 mắt): đặt vào ô trống bất kỳ.
- **Mèo nháy mắt**: gỡ 1 dấu chân của đối thủ.
- Dấu chân nằm trong sequence, được Mèo Canh Gác bảo vệ hoặc đứng trên cỏ mèo thì không bị gỡ, cào, đẩy hay đổi chỗ.
- Lá không dùng được là bài chết: đổi lấy lá mới, 1 lần mỗi lượt. Không còn nước nào thì bỏ lượt.
- Hết giờ, game tự đánh ngẫu nhiên giúp người chơi.

## 🐱 Mèo kỹ năng
| Mèo | Số lá | Kỹ năng |
|---|---|---|
| 🐾 Mèo Cào | 1 | Gỡ 1 dấu chân đối thủ rồi đặt dấu chân của bạn vào đúng ô đó |
| 💨 Mèo Đẩy | 1 | Đẩy 1 dấu chân đối thủ sang 1 ô trống kề bên |
| 🕶️ Mèo Trộm | 1 | Lấy ngẫu nhiên 1 lá thường trên tay đối thủ |
| 🛡️ Mèo Canh Gác | 2 | Bảo vệ 1 dấu chân của bạn (tối đa 2 lần/ván) |
| 💤 Mèo Ngủ | 2 | Chặn 1 ô trống trong 2 vòng |
| 🔄 Mèo Đổi Chỗ | 1 | Đổi chỗ 1 dấu chân của bạn với 1 dấu chân đối thủ |
| 🔮 Mèo Tiên Tri | 1 | Xem bài đối thủ, rồi đánh tiếp |
| ⚡ Mèo Nhanh Nhẹn | 1 | Lượt này được đánh thêm 2 lá |
| 🎣 Mèo Câu Cá | 2 | Rút 2 lá, giữ 1, rồi đánh tiếp |
| 🐟 Mèo Tham Ăn | 1 | Chiếm 1 ô bát cá/hộp giấy: ô đó chỉ tính cho bạn |

## 🗺️ Bản đồ và địa hình
Bản đồ: Phòng khách (gốc), Vườn cỏ mèo, Hồ cá Koi, Kho hộp giấy, Phòng len, Mê cung đá, Ngẫu nhiên.
Mọi bản đồ đều đối xứng tâm để hai bên công bằng.

| Địa hình | Tác dụng |
|---|---|
| 🪨 Tảng đá | Không ai đặt được, chặn đường sequence |
| 💧 Vũng nước | Chỉ Mèo Joker mới đặt được vào |
| 🌿 Cỏ mèo | Dấu chân đứng trên cỏ không thể bị gỡ, cào, đẩy hay đổi chỗ |
| 📦 Hộp giấy | Ô tự do như bát cá |
| 🧶 Cuộn len | Đặt dấu chân vào được đánh thêm 1 lá (1 lần mỗi lượt) |

## Kỹ thuật
Một file `index.html` duy nhất. Game thử kết nối trực tiếp giữa hai máy bằng [PeerJS](https://peerjs.com/) (WebRTC).
Nếu mạng chặn kết nối trực tiếp (4G, mạng công ty…), sau khoảng 6 giây game tự chuyển sang đường dự phòng
đi qua máy chủ MQTT công cộng (EMQX, HiveMQ). Bên cạnh mã phòng có ghi đang dùng đường nào: "trực tiếp" hoặc "qua máy chủ".
