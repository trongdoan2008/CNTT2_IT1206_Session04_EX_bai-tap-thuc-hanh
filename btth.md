# [BTTH] Bài tập thực hành tổng hợp

### **1. Thiết kế giải pháp**

Dữ liệu và yêu cầu của người dùng -> AI kiểm tra, phân tích, tổng hợp và xử lý lỗi theo từng bước -> Kết quả hoàn chỉnh dưới dạng JSON.

### **2. Chuỗi Prompt thực thi**

**Bước 1 – Kiểm tra dữ liệu**

```
Kiểm tra dữ liệu đầu vào, phát hiện dữ liệu thiếu,trùng lặp hoặc sai định dạng
```

**Bước 2 – Phân tích**

```
Phân tích dữ liệu đã làm sạch, phân loại nội dung và không tự suy đoán thông tin
```

**Bước 3 – Tổng hợp**

```
Tổng hợp kết quả từ bước 2,giữ lại thông tin quan trọng và đánh dấu dữ liệu còn thiếu
```

**Bước 4 – Kiểm tra đầu ra**

```
Kiểm tra lỗi và xuất kết quả dưới dạng JSON hợp lệ Nếu lỗi thông báo thay vì làm crash hệ thống
```

### **3. Cơ chế xử lý lỗi**

- Lưu kết quả từng bước 
- Chia nhỏ dữ liệu để 
- Kiểm tra và sửa lỗi JSON
- Tóm tắt thông tin để tiết kiệm token

### **4. Kết quả AI chạy thử**

```
{
  "status": "success",
  "category": "Giao hàng",
  "issue": "Giao hàng chậm 3 ngày",
  "department": "Vận chuyển",
  "priority": "high",
  "errors": [],
  "validated": true
}
```