phần 1: phân tích bảo mật
lỗi tệp login data trên chrome: khi dính infostealer, mã độc đọc thẳng file db chứa pass lưu trên trình duyệt rồi giải mã, đánh cắp toàn bộ tài khoản nhạy cảm (github, aws, stripe).

zero-knowledge & client-side decryption: dữ liệu được mã hoá aes-256 trên máy cá nhân trước khi đẩy lên cloud. máy chủ bitwarden chỉ lưu ciphertext và không bao giờ biết master password-> hacker hack server cũng chỉ đọc được dữ liệu vô nghĩa.

phần 2: chính sách & chuyển đổi
master passphrase chuẩn: dài >= 20 ký tự, kết hợp từ ngẫu nhiên và ký tự đặc biệt. ví dụ: R@inbow-Coffee-Mountain-2026!

cấu hình generator: bật độ dài 24 ký tự, có đủ chữ hoa, chữ thường, số và ký tự đặc biệt.

chống phishing bằng auto-fill: bitwarden chỉ điền khi tên miền khớp tuyệt đối, không bị lừa bởi các trang web giả mạo tinh vi qua mắt thị giác.

quy trình emergency kit: xuất bản file/bản in, niêm phong trong két sắt văn phòng, chỉ trưởng nhóm mới mở để khẩn cấp cứu tài khoản khi trưởng phòng dev gặp sự cố.