phần 1:nhận diện rủi ro & xử lý

tình huống 1: phishing + typosquatting (github.com). chi tiết giả mạo là tên miền sai chính tả và ép nhập lại mật khẩu.
  
  tình huống 2: mã độc infostealer. tắt windows defender giúp mã độc lọt qua, đánh cắp cookie và pass trình duyệt.5 không: tình huống 1 áp dụng không bấm link lạ; tình huống 2 áp dụng không tải phần mềm trôi nổi.4 bước cấp cứu: ngắt mạng ngay ->đổi pass & logout từ thiết bị sạch ->bật 2fa app-> quét virus / cài lại win.

phần 2: 

-password managernguy cơ lộ pass chung: 2 tài khoản còn lại bị hack do credential stuffing.zero-knowledge: mã hóa aes-256 từ máy dev, server chỉ lưu ciphertext nên hacker hack server cũng không đọc được.generator: dài 24 ký tự, bật đủ chữ hoa, chữ thường, số và ký tự đặc biệt.

phần 3:

-2fa github tổ chức sms otp: dễ dính sim swapping và trễ tin nhắn. nên dùng authenticator app (totp).cách bật: settings ->password and security ->enable 2fa ->set up using an app ->quét qr-> nhập mã 6 số.mã khôi phục: in giấy cất két sắt, không chụp ảnh hay lưu file notepad trên máy.

phần 4:

-bảo vệ secrets2 secrets: API_KEY và DB_PASSWORD.code

 an toàn:JavaScriptrequire('dotenv').config();
const API_KEY = process.env.API_KEY;
const DB_PASSWORD = process.env.DB_PASSWORD;
function connectDatabase() {return connect(DB_PASSWORD);}


nội dung file:.env: API_KEY=sk-proj-abc123456789, DB_PASSWORD=SmartCampus@2026.gitignore: .env, node_modules/.env.example: API_KEY=, DB_PASSWORD=

4 bước trước khi push: kiểm tra .env trong .gitignore ->rà code không hardcode-> chạy git status-> push khi repo sạch sẽ.