# BÀI THỰC HÀNH 

## Bước 1: Chỉ ra thông tin nhạy cảm

| Biến | Giá trị | Mức nguy hiểm |
|------|---------|---------------|
| `db_password` | `'rikkei_secret_password_2026'` | Mật khẩu cơ sở dữ liệu thật. Kẻ xấu có thể truy cập, đánh cắp, sửa hoặc xóa dữ liệu của dự án. |
| `api_key` | `'google_gemini_api_abc123'` | Khóa API. Kẻ xấu có thể dùng trái phép dịch vụ, gây tốn chi phí hoặc lạm dụng tài khoản. |

## Bước 2: Làm sạch code và viết prompt an toàn

### 2.1. Code đã làm sạch

```python
def connect_database():
    db_password = '[YOUR_DATABASE_PASSWORD]'
    api_key = '[YOUR_API_KEY]'
    print('Đang kết nối...')
```

### 2.2. Prompt an toàn gửi kèm

```text
Tôi có đoạn code Python dưới đây dùng để kết nối cơ sở dữ liệu. Các giá trị
trong dấu [ ] là biến tượng trưng, không phải dữ liệu thật.

Hãy giúp tôi:
1. Tối ưu cấu trúc code và đặt tên biến cho rõ ràng.
2. Chỉ ra lỗi sai hoặc điểm chưa hợp lý (nếu có).
3. Gợi ý cách quản lý mật khẩu và API key an toàn hơn
   (ví dụ: biến môi trường, file .env).
4. Thêm xử lý lỗi (try/except) khi kết nối thất bại.

Code:

def connect_database():
    db_password = '[YOUR_DATABASE_PASSWORD]'
    api_key = '[YOUR_API_KEY]'
    print('Đang kết nối...')
```

