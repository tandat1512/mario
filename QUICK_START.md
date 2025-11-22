# ⚡ Deploy Nhanh - 5 Phút

## Mục tiêu: Có link chia sẻ cho 2-3 người

---

## 🎯 BƯỚC 1: Backend (Render.com)

1. Vào https://render.com → Login GitHub
2. **New +** → **Web Service**
3. Connect repo → Chọn repo của bạn
4. Điền:
   ```
   Name: beauty-backend
   Build: pip install -r backend/requirements.txt
   Start: cd backend && uvicorn main:app --host 0.0.0.0 --port $PORT
   ```
5. **Create** → Chờ 5 phút → Copy URL backend

---

## 🎯 BƯỚC 2: Frontend (Vercel)

1. Vào https://vercel.com → Login GitHub
2. **Add New** → **Project**
3. Import repo → Chọn repo của bạn
4. Thêm Environment Variables:
   ```
   VITE_BEAUTY_BACKEND = [URL backend từ bước 1]
   GEMINI_API_KEY = [API key của bạn]
   ```
5. **Deploy** → Chờ 2 phút → Copy URL frontend

---

## 🎯 BƯỚC 3: Cập nhật CORS

1. Quay lại Render.com
2. Vào **Environment** tab
3. Sửa `ALLOWED_ORIGINS` = [URL frontend từ bước 2]
4. **Save** → Chờ restart

---

## ✅ XONG!

Link chia sẻ: `https://your-app.vercel.app`

---

## 💡 Tip: Tránh Backend Sleep

Dùng UptimeRobot (miễn phí):
1. https://uptimerobot.com → Đăng ký
2. Add Monitor → HTTP(s) → URL backend
3. Interval: 5 minutes
4. Xong! Backend không bị sleep nữa

