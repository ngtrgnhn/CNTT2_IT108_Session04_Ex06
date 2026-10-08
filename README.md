## **Phần 1: Nhật ký lệnh được trình bày dưới dạng bảng theo đúng yêu cầu:**

| Thứ tự | Lệnh đã gõ | Giải thích |
| ----- | ----- | ----- |
| **1** | `cd ~; mkdir green-iot\bin, green-iot\config, green-iot\data` | Di chuyển nhanh về thư mục Home (`~`) của người dùng và đồng thời tạo thư mục dự án `green-iot` cùng 3 thư mục con `bin`, `config`, `data` chỉ trong một dòng lệnh. PNG |
| **2** | `New-Item green-iot\config\.env -ItemType File` | Tạo tệp tin `.env` bên trong thư mục `config` để chứa thông tin mật khẩu cảm biến. PNG |
| **3** | `Copy-Item "C:\Users\Public\sensor_template.py" .\green-iot\bin\pump_controller.py` | Sao chép file mẫu `sensor_template.py` từ thư mục hệ thống `Public` vào thư mục `bin` và đổi tên thành `pump_controller.py`. |

## **Phần 2: Kiểm thử**

* **Tại sao gõ lệnh dir không thấy file .env?**  
  Các file có tên bắt đầu bằng dấu chấm (.env) mặc định được hệ điều hành Windows phân loại là **tệp tin ẩn (hidden files)** nhằm bảo vệ dữ liệu cấu hình. Do đó, lệnh liệt kê thông thường sẽ không hiển thị chúng.  
* **Cách để nhìn thấy file .env:** Bạn cần thêm tham số \-Force vào câu lệnh liệt kê để hiển thị cả các tệp ẩn:  
* PowerShell

dir \-Force .\\green-iot\\config

*   
* *Cách xác minh:* Tên file .env sẽ hiển thị trong kết quả trả về của terminal.

