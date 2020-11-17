+++
title = "Các bài lab môn Hệ quản trị cơ sở dữ liệu"
date = "2020-09-22"
author = "Lam"
cover = ""
tags = ["dbms", ""]
keywords = ["", ""]
description = ""
showFullContent = false
+++

## Lab1
### 1. Giới thiệu về SQL Server
 - SQL Server hiện có nhiều phiên bản khác nhau. Dưới đây là danh sách các phiên bản cùng với tính năng của từng phiên bản.

| Loại   |  Mô tả  |  
|---|---|
|  Enterprise  | bản cao cấp nhất với đầy đủ tính năng  |
|  Standard | ít tính năng hơn Enterprise, sử dụng khi không cần dùng tới các tính năng nâng cao  |
|  Workgroup | phù hợp cho các công ty lớn với nhiều văn phòng làm việc từ xa  |
| Web | thiết kế riêng cho các ứng dụng web |
| Developer | tương tự như Enterprise nhưng chỉ cấp quyền cho một người dùng duy nhất để phát triển, thử nghiệm, demo. Có thể dễ dàng nâng cấp lên bản Enterprise mà không cần cài lại |
| Express | bản này chỉ dùng ở mức độ đơn giản, tối đa 1 CPU và bộ nhớ 1GB, kích thước tối đa của cơ sở dữ liệu là 10GB (miễn phí, nhẹ, phù hợp để học) |
| Compact | nhúng miễn phí vào các môi trường phát triển ứng dụng web. Kích thước tối đa của cơ sở dữ liệu là 4GB |
| Datacenter | thay đổi lớn trên SQL Server 2008 R2 chính là bản Datacenter Edition. Không giới hạn bộ nhớ và hỗ trợ hơn 25 bản cài |
| Business Intelligence	 | Business Intelligence Edition mới được giới thiệu trên SQL Server 2012. Phiên bản này có các tính năng của bản Standard và hỗ trợ một số tính năng nâng cao về BI như Power View và PowerPivot nhưng không hỗ trợ những tính năng nâng cao về mức độ sẵn sàng như AlwaysOn Availability Groups… |
| Enterprise Evaluation	| bản SQL Server Evaluation Edition là lựa chọn tuyệt vời để dùng được mọi tính năng và có được bản cài miễn phí của SQL Server để học tập và phát triển. Phiên bản này có thời gian hết hạn là 6 tháng từ ngày cài |

### 2. Cài đặt SQLServer

## Lab2.
### 1. Giới thiệu MySQl
MySQL là chương trình dùng để quản lý hệ thống cơ sở dữ liệu (CSDL), trong đó CSDL là một hệ thống lưu trữ thông tin. được sắp xếp rõ ràng, phân lớp ngăn nắp những thông tin mà mình lưu trữ.
### 2. Cài đặt MySQl
- {{< figure src ="/images/Lab2_MySQL.PNG" title = "Lab2.2">}}

# Lab3. Cài đặt MongoDB
### 1. Giới thiệu
MongoDB là một hệ quản trị cơ sở dữ liệu mã nguồn mở, là CSDL thuộc NoSql và được hàng triệu người sử dụng.
MongoDB là một database hướng tài liệu (document), các dữ liệu được lưu trữ trong document kiểu JSON thay vì dạng bảng như CSDL quan hệ nên truy vấn sẽ rất nhanh.

### 2. Cài đặt MongoDB
- {{< figure src ="/images/Lab3_MongoDB.PNG" title = "Lab3.2.1">}}
- {{< figure src ="/images/Lab3_MongoDB.2.PNG" title = "Lab3.2.2">}}

# Lab5. Cài đặt MongoDB trên Docker:
Cài đặt mongoDB trong Docker thông qua lệnh: docker pull mongo
Kiểm tra các image trong Docker:
- {{< figure src ="/images/Lab4+5.PNG" title = "Lab5.1">}}

Chạy Docker conatainer mongo
- {{< figure src ="/images/Lab5_DockerContainer.PNG" title = "Lab5.2">}}

Khởi động container:
- {{< figure src ="/images/Lab5_DockerExecution.PNG" title = "Lab5.2">}}

# Lab6. Cài đặt MySQL trên Docker:
- {{< figure src ="/images/Lab6_mysql.PNG" title = "Cài đặt MySQL trong Docker thông qua lệnh: docker pull mysql">}}

- {{< figure src ="/images/Lab8_dockernetwork.PNG" title = "Việc tạo Docker network giúp cho các Docker container trong cùng 1 network có thể giao tiếp với nhau thông qua container name">}}

- {{< figure src ="/images/Lab8_dockercontainer.PNG" title = "Khởi tạo Docker container từ Docker image của MySQL">}}
trong đó:

--name learn_mysql: tên của container. Tên này sẽ được sử dụng ở bước sau, khi chúng ta khới tạo container chạy phpMyAdmin.

--network mysql: đặt container này trong network mysql vừa được tạo ở bước 1.

-v /home/moe/mysql_data:/var/lib/mysql : Volume dữ liệu từ container ra bên ngoài thư mục mysql_data mà chúng ta vừa tạo.

-e MYSQL_ROOT_PASSWORD=123: đặt password cho user root. Mỗi một MySQL server khi được khởi tạo đều sẽ có một user root ban đầu.


- {{< figure src ="/images/Lab8_dockercontainerphp.PNG" title = "Khởi tạo Docker container từ Docker image của phpMyAdmin">}}
trong đó:

--name myadmin: tên container.

--network mysql: đặt container này vào trong network mysql. Lúc này 2 container chạy phpMyAdmin và MySQL đều ở trong cùng 1 network.

-e PMA_HOST=learn_mysql: địa chỉ IP của MySQL server. Vì chúng ta đã đặt 2 container chạy phpMyAdmin và MySQL trong cùng 1 network (mysql) nên chúng ta có thể dùng tên container chạy MySQL (learn_mysql) cho biến môi trường này.

-p 8081:80: mapping cổng 80 của container với cổng 8081 của máy host.

### Truy cập localhost 8081
- {{< figure src ="/images/Lab8_localhost.PNG">}}


# Lab7. Sử dụng DDL định nghĩa dữ liệu cho đối tượng Sinh Viên
### 1. Sử dụng MySQL:
- {{< figure src ="/images/Lab7_MySQL.PNG" title = "Lab7.1.1">}}
- {{< figure src ="/images/Lab7_MySQL.2.PNG" title = "Lab7.1.2">}}

### 2. Sử dụng MongoDB:

- {{< figure src ="/images/Lab7_MongoDB.PNG" title = "Lab7.2">}}

# Lab8. Tạo 10 mẫu tin (nhập dữ liệu) cho 10 sinh viên. Sau đó thực hiện các thao tác CRUD (Create, Read, Update, Delete) trên dữ liệu mẫu.
### 1. MySQL:
#### Create:
- {{< figure src ="/images/Lab8_MySQL_C.PNG" title = "Lab8.1">}}

#### Read: 
Sử dụng lệnh query: select * from sinhvien
- {{< figure src ="/images/Lab8_MySQL_R.PNG" title = "Lab8.2">}}


#### Update:
Sử dụng lệnh query: update sinh vien set DienThoai='1593572468' where Hoten='long'
- {{< figure src ="/images/Lab8_MySQL_LongBefore.PNG" title = "Lab8.3.1">}}
- {{< figure src ="/images/Lab8_MySQL_LongAfter.PNG" title = "Lab8.3.2">}}


#### Delete:
Sử dụng lệnh query: delete from sinhvien where MSSV='000'
Kết quả sau khi xóa: Chỉ còn lại 8 sinh viên:
- {{< figure src ="/images/Lab8_MySQL_Delete.PNG" title = "Lab8.4">}}

### 2. MongoDB:
#### Create:
- {{< figure src="/images/Lab8_mongoC.PNG">}}
#### Read: 
- {{< figure src="/images/Lab8_mongoR.PNG">}}

#### Update:

#### Delete:
- {{< figure src="/images/Lab8_mongoD.PNG">}}

# Lab9&10:
### MongoDB:
#### Create:
- {{< figure src="/images/Lab9_InsertCode.PNG" title="Code tạo">}}
- {{< figure src="/images/Lab9_Insert.PNG" title="Kết quả tạo">}}

#### Read: 
- {{< figure src="/images/Lab9_Read.PNG" title="Code Đọc">}}
- {{< figure src="/images/Lab9_Read.PNG" title="Kết quả Đọc">}}

#### Update:
- {{< figure src="/images/Lab9_UpdateCode.PNG" title="Code cập nhật">}}
- {{< figure src="/images/Lab9_UpdateValue.PNG" title="Kết quả cập nhật">}}

#### Delete:
- {{< figure src="/images/Lab9_DeleteCode.PNG" title="Code xóa">}}
- {{< figure src="/images/Lab9_DeleteResult.PNG" title="Kết quả xóa">}}

### MySQL:
#### Create:
- {{< figure src="/images/Lab9_mysqlCC.PNG" title="Code tạo sql">}}
- {{< figure src="/images/Lab9_mysqlCR.PNG" title="Kết quả tạo sql">}}

#### Read: 
- {{< figure src="/images/Lab9_mysqlRC.PNG" title="Code Đọc sql">}}
- {{< figure src="/images/Lab9_mysqlCR.PNG" title="Kết quả Đọc sql">}}

#### Update:
- {{< figure src="/images/Lab9_UC.PNG" title="Code cập nhật sql">}}
- {{< figure src="/images/Lab9_UB.PNG" title="Kết quả trước cập nhật sql">}}
- {{< figure src="/images/Lab9_UA.PNG" title="Kết quả cập nhật sql">}}

#### Delete:
- {{< figure src="/images/Lab9_mysqlDC.PNG" title="Code xóa sql">}}
- {{< figure src="/images/Lab9_DB.PNG" title="Kết quả trước khi xóa sql">}}
- {{< figure src="/images/Lab9_DA.PNG" title="Kết quả sau khi xóa sql">}}