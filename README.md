# WEB - BASED APP DEVELOPMENT
## THÔNG TIN CÁ NHÂN
#### Họ và tên: Nguyễn Trung Hiếu
#### Mã sinh viên: K225480106019
#### Lớp: K58KTP
## BÀI TẬP VỀ NHÀ 01
## TÓM TẮT YÊU CẦU:
### TẠO SOLUTION GỒM CÁC PROJECT SAU:
#### 1. Class library (.NET Framework 2.0)
- DLL đa năng bắt buộc sử dụng .NET Framework 2.0: giải bài toán bất kỳ, độc lạ càng tốt, phải có dấu ấn cá nhân trong kết quả, biên dịch ra DLL.
- DLL độc lập — không đọc/ghi file, nó nhận input truyền vào thuộc tính của nó, và trả về dữ liệu thông qua thuộc tính khác, hoặc thông qua giá trị trả về của hàm.
#### 2. Console App (.NET Framework 2.0)
- Bắt buộc sử dụng .NET Framework 2.0
- Sử dụng được DLL trên: nhập được input, gọi DLL, hiển thị kết quả, phải có dấu ấn cá nhân.
- Biên dịch ra EXE.
#### 3. Windows Form Application
- Bắt buộc sử dụng .NET Framework 2.0
- Sử dụng được DLL đa năng trên, kéo các control vào để có thể lấy đc input, gọi DLL truyền input để lấy được kết quả, hiển thị kết quả ra window form, phải có dấu ấn cá nhân
- Biên dịch ra EXE.
#### 4. WEB
- Web đơn giản, bắt buộc sử dụng .NET Framework 2.0
- Sử dụng web server là IIS, dùng file hosts để tự tạo domain, gắn domain này vào iis.
- File index.html có sử dụng html css js để xây dựng giao diện nhập được các input cho bài toán, dùng mã js để tiền xử lý dữ liệu, js để gửi lên backend.
- Backend là api.aspx, trong code của api.aspx.cs thì lấy được các input mà js gửi lên, rồi sử dụng được DLL đa năng trên. Kết quả gửi lại json cho client, js phía client sẽ nhận được json này hậu xử lý để thay đổi giao diện theo dữ liệu nhận được.
- Project web này biên dịch ra DLL, phải kết hợp với IIS mới chạy được.
## BÀI TOÁN: Trang Web "Độ tương thích tình yêu" (LOVE COMPATIBILITY) bằng chỉ số phần trăm (0-100) giữa hai tên người.
## CÁC BƯỚC THỰC HIỆN SOLUTION:
### Bước 1: Tạo Solution
- Mở Visual Studio 2022
- File -> New -> Project
- Gõ Blank Solution trong thanh tìm kiếm rồi chọn mục đó, bấm Next
- Đặt tên Solution và tạo: LOVE_COMPATIBILITY -> Create
<img width="2020" height="1342" alt="Screenshot 2025-09-27 230331" src="https://github.com/user-attachments/assets/5b542a78-9ef5-451f-a486-ba492574dd2d" />

### Bước 2: Tạo Class Library
- Trong cửa sổ Solution Explorer, click chuột phải vào tên solution vừa tạo, chọn Add -> New Project.
- Tìm kiếm: Class Library (.NET Framework) rồi chọn Next
- Đặt tên cho Project: Love_Compatibility
- Ở mục Framework chọn .NET Framework 2.0 -> Create
<img width="3071" height="1825" alt="Screenshot 2025-09-27 233521" src="https://github.com/user-attachments/assets/46168f87-f4e0-430b-8941-0154bab5d667" />

DLL được tạo ở bước này sẽ được dùng cho Console App, WinForm và Web.
#### Build DLL
- Nháy chuột phải vào project -> Build (hoặc Ctrl+Shift+B).
- Kết quả: Trong folder bin\Debug (hoặc Release), sẽ có file Love_Compatibility.dll. Đây là DLL độc lập, copy dùng ở các project khác.
<img width="3063" height="1829" alt="Screenshot 2025-09-27 235518" src="https://github.com/user-attachments/assets/36a2eac6-d0c4-418f-8856-d1df64d081a6" />
