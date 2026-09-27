# 🐾 Sequence Mèo

Game **Sequence** chủ đề mèo, chơi online 1 đấu 1 ngay trên trình duyệt, không cần server hay tài khoản.

## Cách chơi với bạn bè
1. Mở trang game, nhập tên, bấm **Tạo phòng**.
2. Gửi **mã phòng** hoặc **link** cho bạn bè; bạn bè nhập tên và bấm **Vào phòng**.
3. Người tạo phòng (chủ phòng) phải **giữ tab mở** suốt ván, vì máy chủ phòng giữ trạng thái ván chơi.

## Luật
- Chọn 1 lá bài trên tay, bấm vào 1 trong 2 ô có lá đó để đặt dấu chân 🐾.
- 5 dấu chân liên tiếp (ngang/dọc/chéo) = 1 sequence. 4 ô bát cá ở góc tính cho cả hai bên.
- Có **2 sequence** là thắng. Hai sequence được dùng chung tối đa 1 ô.
- **J♦ J♣** (mèo 2 mắt): đặt vào ô trống bất kỳ.
- **J♠ J♥** (mèo nháy mắt): gỡ 1 dấu chân của đối thủ (trừ dấu đã nằm trong sequence).
- Bài chết (cả 2 ô đã có chip): đổi lấy lá mới, 1 lần mỗi lượt.

## Kỹ thuật
Một file `index.html` duy nhất. Kết nối P2P bằng [PeerJS](https://peerjs.com/) (WebRTC). Một số mạng
(4G, mạng công ty có NAT chặt) có thể không kết nối được do không có TURN server; khi đó thử đổi mạng khác (Wi-Fi).
