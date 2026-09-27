# 🐾 Sequence Mèo

Game **Sequence** chủ đề mèo, chơi online 1 đấu 1 ngay trên trình duyệt, không cần server hay tài khoản.

## Cách chơi với bạn bè
1. Mở trang game, nhập tên, bấm **Tạo phòng**.
2. Gửi **mã phòng** hoặc **link** cho bạn bè; bạn bè nhập tên và bấm **Vào phòng**.
3. Người tạo phòng (chủ phòng) phải **giữ tab mở** suốt ván, vì máy chủ phòng giữ trạng thái ván chơi.

## Luật
- Mỗi người cầm 3 lá. Chọn 1 lá trên tay, các ô đặt được sẽ sáng lên, bấm vào ô để đặt dấu chân 🐾.
- 5 dấu chân liên tiếp (ngang/dọc/chéo) = 1 sequence. 4 ô bát cá ở góc tính cho cả hai bên.
- Có **2 sequence** là thắng. Hai sequence được dùng chung tối đa 1 ô.
- **Mèo Joker** (lá đặc biệt, mèo mở 2 mắt): đặt vào ô trống bất kỳ.
- **Mèo nháy mắt** (lá đặc biệt): gỡ 1 dấu chân của đối thủ (trừ dấu đã nằm trong sequence).
- Bài chết (cả 2 ô đã có chip): đổi lấy lá mới, 1 lần mỗi lượt.

## Kỹ thuật
Một file `index.html` duy nhất. Game thử kết nối trực tiếp giữa hai máy bằng [PeerJS](https://peerjs.com/) (WebRTC).
Nếu mạng chặn kết nối trực tiếp (4G, mạng công ty…), sau khoảng 6 giây game tự chuyển sang đường dự phòng
đi qua máy chủ MQTT công cộng (EMQX, HiveMQ). Bên cạnh mã phòng có ghi đang dùng đường nào: "trực tiếp" hoặc "qua máy chủ".
