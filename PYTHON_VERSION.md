# 🐍 Yêu Cầu Phiên Bản Python

## Phiên Bản Khuyến Nghị

**Python 3.11.9** (hoặc 3.11.x) - **Đã được cấu hình trong dự án**

## Yêu Cầu Tối Thiểu

**Python 3.9** - Do `numpy>=1.24.0` yêu cầu Python >= 3.9

## Tại Sao Python 3.11.9?

### ✅ Tương Thích Hoàn Toàn
- ✅ **numpy>=1.24.0,<2.0.0**: Hỗ trợ Python 3.9-3.12
- ✅ **pydantic>=2.0.0**: Hỗ trợ Python 3.8+, hoạt động tốt nhất từ 3.9+
- ✅ **fastapi>=0.104.0**: Hỗ trợ Python 3.8+
- ✅ **opencv-python>=4.8.0**: Hỗ trợ Python 3.8+
- ✅ **mediapipe>=0.10.0**: Hỗ trợ Python 3.8+
- ✅ **pillow>=10.0.0**: Hỗ trợ Python 3.8+
- ✅ **uvicorn[standard]>=0.24.0**: Hỗ trợ Python 3.8+

### 🚀 Hiệu Suất
- Python 3.11 nhanh hơn 10-60% so với Python 3.9/3.10
- Tối ưu hóa tốt hơn cho xử lý ảnh và AI

### 🔒 Ổn Định
- Python 3.11 là phiên bản ổn định, được hỗ trợ tốt
- Tương thích với các nền tảng deploy (Render.com, Heroku, etc.)

## Cấu Hình Hiện Tại

Dự án đã được cấu hình với Python 3.11.9 trong:
- `runtime.txt`: `python-3.11.9`
- `backend/runtime.txt`: `python-3.11.9`
- `render.yaml`: `PYTHON_VERSION: 3.11.9`

## Kiểm Tra Phiên Bản Python

```bash
# Kiểm tra phiên bản hiện tại
python --version

# Hoặc
python3 --version
```

## Cài Đặt Python 3.11.9

### Windows
1. Tải từ: https://www.python.org/downloads/release/python-3119/
2. Chọn "Add Python to PATH" khi cài đặt

### macOS
```bash
# Sử dụng Homebrew
brew install python@3.11

# Hoặc pyenv
pyenv install 3.11.9
pyenv global 3.11.9
```

### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install python3.11 python3.11-venv python3.11-pip
```

## Tạo Virtual Environment

```bash
# Tạo venv với Python 3.11
python3.11 -m venv venv

# Kích hoạt venv
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Cài đặt dependencies
pip install -r backend/requirements.txt
```

## Lưu Ý

- ⚠️ **Không sử dụng Python 3.8** - NumPy 1.24+ không hỗ trợ
- ⚠️ **Không sử dụng Python 3.13+** - Một số thư viện có thể chưa hỗ trợ đầy đủ
- ✅ **Python 3.9-3.12** đều hoạt động tốt
- ✅ **Python 3.11.9** là lựa chọn tối ưu cho dự án này

## Troubleshooting

### Lỗi: "numpy requires Python >= 3.9"
→ Cài đặt Python 3.9 hoặc cao hơn

### Lỗi: "No module named 'cv2'"
→ Cài đặt lại: `pip install opencv-python`

### Lỗi khi deploy trên Render.com
→ Đảm bảo `runtime.txt` có `python-3.11.9`

