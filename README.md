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
- Sử dụng được DLL trên: nhập được input, gọi DLL, hiển thị kết quả, phải có dấu án cá nhân.
- Biên dịch ra EXE.
#### 3. Windows Form Application
- Bắt buộc sử dụng .NET Framework 2.0
- Sử dụng được DLL đa năng trên, kéo các control vào để có thể lấy đc input, gọi DLL truyền input để lấy đc kq, hiển thị kq ra window form, phải có dấu án cá nhân
- Biên dịch ra EXE.
#### 4. WEB
- Web đơn giản, bắt buộc sử dụng .NET Framework 2.0
- Sử dụng web server là IIS, dùng file hosts để tự tạo domain, gắn domain này vào iis.
- File index.html có sử dụng html css js để xây dựng giao diện nhập được các input cho bài toán, dùng mã js để tiền xử lý dữ liệu, js để gửi lên backend.
- Backend là api.aspx, trong code của api.aspx.cs thì lấy được các input mà js gửi lên, rồi sử dụng được DLL đa năng trên. Kết quả gửi lại json cho client, js phía client sẽ nhận được json này hậu xử lý để thay đổi giao diện theo dữ liệu nhận được.
- Project web này biên dịch ra DLL, phải kết hợp với IIS mới chạy được.
## BÀI TOÁN: 
