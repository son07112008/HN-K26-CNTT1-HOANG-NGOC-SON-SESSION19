phần 1: phân tích
4 secrets lộ: openai api key, steam api key, mongo uri, jwt secret->nguy cơ bị bot quét mất tiền, lộ database, giả mạo quyền admin.

vì sao phải revoke ngay: bot scraper cào trong 3-5 giây đầu, xóa commit hay đổi sang private cũng không xóa được lịch sử git đã bị lưu từ trước.

phần 2: sửa lỗi
tệp .env:

Đoạn mã
OPENAI_API_KEY=sk-proj-998822abcfed7711aaff00998877665544332211
STEAM_WEB_API_KEY=STEAM_SECRET_KEY_882910AAFFBBDD
MONGO_URI=mongodb+srv://admin_root:SuperSecretPass2026@cluster0.pixelforge.net/cyberrealm_db
JWT_SECRET=pixel_forge_super_private_token_key_9988
mã server.js an toàn:

JavaScript
require('dotenv').config();
const express = require('express');
const app = express();

const OPENAI_API_KEY = process.env.OPENAI_API_KEY;
const STEAM_WEB_API_KEY = process.env.STEAM_WEB_API_KEY;
const MONGO_URI = process.env.MONGO_URI;
const JWT_SECRET = process.env.JWT_SECRET;

app.listen(3000, () => console.log('Game Server running on port 3000'));
tệp .gitignore:

Đoạn mã:
.env
node_modules/
tệp .env.example:

Đoạn mã:
OPENAI_API_KEY=your_openai_api_key_here
STEAM_WEB_API_KEY=your_steam_api_key_here
MONGO_URI=your_mongodb_connection_string_here
JWT_SECRET=your_jwt_secret_key_here