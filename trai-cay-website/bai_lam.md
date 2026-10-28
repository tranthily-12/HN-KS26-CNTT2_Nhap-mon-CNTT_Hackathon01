# BÀI LÀM – HACKATHON 01

- **Mã đề:** 17
- **Họ tên:** Trần Thị Lý
- **Lớp:** HN-KS26-CNTT2
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# pwd
# ls -Force 
# mv .\nguon_hang.txt .\docs\  
# mv .\logo_trai_cay_sach.png .\media\
# rm .\temp_252.tmp
# cd .\logs\
# ls -Force 
# cd ..
# Get-ChildItem -Recurse -Force

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
  Directory: C:\Users\fpt yen thanh\Downloads\starter-kit (1)\starter-kit\trai-cay-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026   1:35 PM                backup
d-----        10/28/2026   1:37 PM                data
d-----        10/28/2026   1:50 PM                docs
d-----        10/28/2026   2:22 PM                logs
d-----        10/28/2026   1:42 PM                media
------        10/27/2026   1:32 AM             70 .env
-a----        10/28/2026   1:33 PM           2264 bai_lam.md
-a----        10/28/2026   2:07 PM            941 README.md


PS C:\Users\fpt yen thanh\Downloads\starter-kit (1)\starter-kit\trai-cay-website>  Get-ChildItem -Recurse -Force


    Directory: C:\Users\fpt yen thanh\Downloads\starter-kit
    (1)\starter-kit\trai-cay-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026   1:35 PM                backup
d-----        10/28/2026   1:37 PM                data
d-----        10/28/2026   1:50 PM                docs
d-----        10/28/2026   2:22 PM                logs
d-----        10/28/2026   1:42 PM                media
------        10/27/2026   1:32 AM             70 .env
-a----        10/28/2026   1:33 PM           2264 bai_lam.md
-a----        10/28/2026   2:07 PM            941 README.md


    Directory: C:\Users\fpt yen thanh\Downloads\starter-kit
    (1)\starter-kit\trai-cay-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           6095 ban_trai_cay_
                                                  thang_7.xlsx


    Directory: C:\Users\fpt yen thanh\Downloads\starter-kit
    (1)\starter-kit\trai-cay-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM             66 nguon_hang.tx
                                                  t


    Directory: C:\Users\fpt yen thanh\Downloads\starter-kit
    (1)\starter-kit\trai-cay-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/28/2026   2:17 PM             40 auto_report.t
                                                  xt
-a----        10/28/2026   1:47 PM            580 daily_report.
                                                  txt
-a----        10/28/2026   2:24 PM           1413 fruit.log
-a----        10/28/2026   2:22 PM             46 tong_hop.txt


    Directory: C:\Users\fpt yen thanh\Downloads\starter-kit
    (1)\starter-kit\trai-cay-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           7054 logo_trai_cay
                                                  _sach.png

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
# Get-Content .\logs\fruit.log | Select-String "ERROR" > logs/daily_report.txt
# Get-Content .\logs\daily_report.txt -Head 2

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-07-28 09:31:32 [ERROR] Thanh toan bi tu choi
2026-07-28 09:40:32 [ERROR] Het thoi gian cho (timeout)

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
#  .\auto_report.ps1
```

### Kết quả hiển thị

```text


```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
# Ghi lệnh vào đây (xoá dòng này)

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
Count    : 5

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
#  New-Item logs/tong_hop.txt
# Get-Content .\logs\fruit.log | Select-String "WARNING" >> .\logs\fruit.log
# (Get-Content .\logs\fruit.log | Select-String "ERROR" | Measure-Object).Count  >> .\logs\tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===

2026-07-28 09:37:32 [WARNING] Don giao trong gio cao diem
2026-07-28 10:07:32 [WARNING] Don giao trong gio cao diem
2026-07-28 10:13:32 [WARNING] Don giao trong gio cao diem


5


```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_trai_cay_thang_7.xlsx`, không cần ghi vào đây.
