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
## BÀI TOÁN: Trang Web "Độ tương thích tình yêu" (LOVE COMPATIBILITY CALCULATOR) bằng chỉ số phần trăm (0-100) giữa hai tên người.
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

### Bước 3: Tạo Console App 
Theo yêu cầu, cần phải:
- Sử dụng DLL từ Project 1 (LoveCompatibility.dll) để tính độ tương thích tình yêu.
- Nhập input từ console, gọi DLL, hiển thị kết quả.

Các bước thực hiện:
- Tạo Project: tương tự bước 2, Đặt tên project là LoveCompatibilityConsole -> Create
<img width="2028" height="1352" alt="Screenshot 2025-09-28 000209" src="https://github.com/user-attachments/assets/7dd0dd49-6e3d-48fd-974e-9ec5bd2023a3" />

- Sau khi tạo xong, nháy chuột phải vào project chọn Add -> Reference -> Project -> Love_Compatibility (Project 1) -> OK.
<img width="1605" height="1112" alt="Screenshot 2025-09-28 000629" src="https://github.com/user-attachments/assets/9fbc4fc1-5c56-43ca-8299-1a2512ed4991" />

#### Build & Run
- Click chuột phải vào Project LoveCompatibilityConsole chọn Build
- Run code (F5 hoặc Ctrl + F5).
<img width="3071" height="1824" alt="Screenshot 2025-09-28 001825" src="https://github.com/user-attachments/assets/457869de-08e4-4e52-8e25-983c5c4cebf7" />
<img width="3064" height="1827" alt="Screenshot 2025-09-28 002600" src="https://github.com/user-attachments/assets/be4f402b-d836-4492-a91a-216fb9fa3bf1" />

#### Sau khi build, file .exe sẽ được tạo.
### Bước 4: Tạo Windows Form Application
Theo yêu cầu, ứng dụng này phải:
- Sử dụng DLL từ Project 1 (LoveCompatibility.dll) để tính độ tương thích tình yêu.
- Có giao diện với các control (textbox, button, label) để nhập input, gọi DLL, và hiển thị kết quả.

Dựa trên DLL đã tạo, em đã thiết kế một Windows Form đơn giản với giao diện cơ bản và thêm chút dấu ấn:
- Tạo project mới tương tự như hai bước trên, đặt tên là LoveCompatibilityWinForm
- Nháy chuột phải vào project vừa tạo -> Add -> Reference -> Project -> Love_Compatibility (Project 1) -> OK.
#### Thiết kế giao diện:
<img width="3071" height="1831" alt="Screenshot 2025-09-28 012840" src="https://github.com/user-attachments/assets/aeb2db7c-a00a-43a4-b357-26b15d25ed5d" />

#### Build & Run:
<img width="3071" height="1830" alt="Screenshot 2025-09-28 012801" src="https://github.com/user-attachments/assets/1b26446f-92b9-4488-a5c5-95a650d766ae" />
<img width="3071" height="1825" alt="Screenshot 2025-09-28 013123" src="https://github.com/user-attachments/assets/8b7ee1ee-ba22-4f79-957e-2c4fd6554cda" />

### Bước 5: Tạo Web
- Tạo project chọn Add -> New Project -> ASP.NET Web Application (.NET Framework) -> Đặt tên là LoveCompatibilityWeb
- Chọn .NET Framework 2.0 -> create
- Trong template, chọn Empty Web Application (không dùng MVC) -> OK.
<img width="2055" height="1380" alt="Screenshot 2025-09-28 084517" src="https://github.com/user-attachments/assets/d8f46273-6e0a-424e-b0c7-5c181637d597" />

- Sau khi tạo xong, thêm reference đến dll.
#### Tạo file index.html
- Nháy chuột phải Project -> Add -> New Item -> HTML Page -> Đặt tên index.html
- Tạo file index.html với HTML + CSS để hiển thị giao diện, và JavaScript để xử lý sự kiện.
#### Tạo file api.aspx
- Nháy chuột phải Project -> Add -> New Item -> WebForm -> Đặt tên api.aspx
- Mở api.aspx, để trống nội dung markup, thêm code cho file.
#### Cấu hình IIS và domain
- Mở Control Panel -> Programs -> Turn Windows features on or off -> Tick Internet Information Services -> OK.
- Mở IIS Manager -> Add Website -> Đặt:
  - Sitename: LoveCompatibilityWeb
  - Physical path: thư mục LoveCompatibilityWeb.
  - Binding: type: http ; IP Address: All Unassigned ; Port: 80.
  - Hostname: love.compatibility.local -> OK.
<img width="1168" height="1336" alt="image" src="https://github.com/user-attachments/assets/7580deaa-93f0-4341-a92f-0270544cb4c9" />

- Thêm domain vào file hosts:
  - Notepad -> Run as Administrator
  - Open file C:\Windows\System32\drivers\etc\hosts
  - Thêm dòng 127.0.0.1 love.compatibility.local
<img width="1804" height="1019" alt="image" src="https://github.com/user-attachments/assets/0444942a-e220-4b28-8bdb-dc6e90def21d" />

- Cấu hình Application Pool:
<img width="2283" height="1303" alt="image" src="https://github.com/user-attachments/assets/a56cc44e-78cd-41e3-aa06-16062608cd29" />

- Đảm bảo trong thư mục LoveCompatibilityWeb\bin phải có file dll của Project 1 và Project 4.
- Mở trình duyệt gõ: htttp://love.compatibility.local để chạy web
- 
