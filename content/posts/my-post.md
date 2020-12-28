+++
title = "Các bài lab môn phát triển ứng dụng web"
date = "2020-09-22"
author = "Lam"
cover = ""
tags = ["ptudweb", ""]
keywords = ["", ""]
description = ""
showFullContent = false
+++

## Lab 1. Hiểu về DNS
### 1. DNS là viết tắt của các chữ nào? 

Domain Name System: Hệ thống tên miền hay Hệ thống phân giải (resolve) tên miền. 

### 2. DNS dùng để làm gì?
DNS dùng để lưu trữ các tên miền (domain name, ví dụ www.google.com), cung cấp dịch vụ chuyển đổi từ địa chỉ dạng chuỗi (tên miền) sang địa chỉ dạng số (IP) và ngược lại (ví dụ www.google.com <> 216.58.221.228).

### 3. Hãy truy cập 3 trang web mà không cần dùng tới tên miền (domain name)?

### 4. Tên miền cấp 1, cấp 2, cấp 3 là gì? cho ví dụ mỗi loại?
Tên miền cấp 1 cũng là tên miền quốc tế, được dùng chung cho nhiều quốc gia, mỗi tên miền đại diện cho một lĩnh vực, một ngành nghề, hay một khu vực địa lý. Ví dụ: .com, .net, .org, .mil, .edu, .gov, .asia, .eu

Tên miền cấp 2 cũng là tên miền quốc gia, thông thường mỗi quốc gia sẽ có một tên miền riêng, gồm hai kí tự. Ví dụ: .vn (Việt Nam), .cn (Trung Quốc), .uk (Anh), .us (Mỹ).

Tên miền cấp 3 là tên miền kết hợp giữa tên miền cấp 2 và tên miền cấp 1. Ví dụ: .com.vn, .edu.vn, .edu.uk, .com.us

### 5. Tên miền quốc tế là gì? cho 3 ví dụ?

Tên miền quốc tế: do Trung tâm quản lý tên miền quốc tế cấp, ví dụ thường có đuôi là .com, .net, .biz, .info, .org

### 6. Tên miền “nội địa” hay quốc gia là gì? cho 3 ví dụ?
Tên miền quốc gia (nội địa): do Trung tâm quản lý tên miền của mỗi quốc gia quản lý. Ví dụ tên miền của Việt Nam có đuôi dạng .vn, .com.vn, edu.vn, gov.vn. Các tên miền này do VNNIC quản lý.

### 7. DNS server addresses trong cạc mạng máy tính dùng để làm gì? Tại sao lại có Preferred DNS server/Alternate DNS server?

Để thiết lập địa chỉ của máy phân giải tên miền. Một  cái chính và một cái dự phòng.

### 8. Trong card mạng, không điền thông tin trong DNS server, có truy cập được trang web không? chứng minh?

– Card mạng sẽ tự động chuyển sang chế độ lấy DNS server address tự động.


– Nếu cố tình gán một DNS server address không tồn tại thì không thể truy cập trang web.

### 9. “8.8.8.8” là gì?

Là DNS server address của Google

### 10. Sau khi người dùng gõ vào trình duyệt https://www.w3schools.com/ , gõ phím Enter.Viết lại quá trình một trình duyệt lấy trang web về?

– Dựa vào thông tin DNS server address, gửi một gói tin để phân giải tên trang web sang IP.

– Gửi một gói tin yêu cầu nội dung trang web (index.html) tới Web server.

– Web server gửi nội dung trang web về cho máy client.


– Máy client thông dịch (biên dịch) mã nguồn của trang web (HTML, CSS, JavaScript) rồi hiển thị lên trình duyệt.

### 11. Thử cấu hình DNS server: sửa tập tin hosts để khi người dùng truy cập trang tuoitre.vn, nội dung trình duyệt sẽ hiển thị thông báo lỗi “không thể truy cập được trang tuoitre.vn”.


Ví dụ: 1.1.1.1  tuoitre.vn

– Thông thường trong một địa chỉ IP sẽ được đặt nhiều tên miền trên đó (sẽ tìm hiểu kĩ hơn ở phần thiết lập web server), vì vậy, sẽ thực hiện việc chuyển hướng trang web sau phần tìm hiểu về web server.

Ví dụ một phần trong tập tin hosts:

127.0.0.1 www.ngvteo.com
127.0.0.1 thuatngucntt.com
127.0.0.1 localhost

Ví dụ một đoạn mã cấu hình cho một trang web trên Apache:

 <VirtualHost *:80>
    DocumentRoot "E:\WebRootYersin\NVTeo"
    ServerName www.ngvteo.com

</VirtualHost>

## Lab 2. Đăng ký tên miền miễn phí

### 1. Tại sao lại phải đăng ký tên miền?

– Xây dựng và bảo vệ thương hiệu

– Xây dựng website để quản lý, dạy học, làm việc, làm thương mại, quảng cáo, quảng bá thương hiệu

### 2. Đăng ký 3 tên miền miễn phí trên 3 hệ thống khác nhau?

Một số trang web tham khảo:

– pages.github.com

– 000webhostapp.com

– wordpress.com

– my.noip.com

– my.freenom.com

– somee.com

– blogspot.com

– biz.nf

/static

## Lab 3. Đăng ký tên miền có phí

### 1. Tại sao nên đăng kí tên miền có phí?

Một số lý do:

– Tên miền miễn phí chỉ sử dụng được trong một khoảng thời gian nhất định, có thể bị mất bất cứ khi nào

– Tên miền miễn phí không nhận được hỗ trợ kĩ thuật

### 2. Khảo sát bảng giá khi đăng kí tên miền có phí từ 6 nhà cung cấp dịch vụ (3 nhà cung cấp trong nước, 3 nhà cung cấp nước ngoài)?


### 3. Liệt kê các bước (thủ tục) để có thể đăng kí tên miền có phí?

### Lab 4. Web server:
## Web server:
- Web Client là một chương trình có thể giao tiếp với Web Server, gửi yêu cầu và nhận thông tin từ Web Server, sau đó xử lý các thông tin nhận được để hiển thị hoặc phục vụ các mục đích khác. Trình duyệt chính là một Web Client.

- Web Server là một máy tính, cung cấp các dịch vụ WWW trên Internet. Web Server gồm có: phần cứng, hệ điều hành, phần mềm Web Server, và nội dung của website.

Theo wiki (https://en.wikipedia.org/wiki/Web_server), đôi khi khái niệm Web Server còn được sử dụng để chỉ một phần mềm, mà nó hiện thực hóa giao thức HTTP (ví dụ, phần mềm Web Server).

- {{< figure src="/images/WebServer.jpg" title="Web Server">}}

Diễn giải hình trên:

- Nhà phát triển web (Web Developer) thiết kế và lập trình ra Website

- Sau khi tạo ra Website, Web Developer sẽ đăng kí một tên miền có tên www.test.com, thuê một không gian đĩa cứng trên Web Server để đặt Website của mình

- Dùng giao thức FTP để chuyển Website (từ máy cục bộ) lên Web Server

- Cuối cùng, người dùng (client) có thể truy cập đến trang www.test.com bằng cách gõ vào trình duyệt đường dẫn (URL) là http://www.test.com và bấm Enter

- Trình duyệt sẽ gửi một HTTP REQUEST tới Web Server để yêu cầu nội dung trang web

- Web Server sẽ gửi nội dung trang web (HTML) về cho trình duyệt bằng HTTP RESPONSE

Như vậy, chức năng của Web Server là: lưu trữ, xử lý và cung cấp trang web tới người dùng. Giao thức được sử dụng để giao tiếp giữa Web Server và Web Client là HTTP hoặc HTTPS.

Phần dưới đây sẽ tìm hiểu về các thành phần liên quan đến Web Server, gồm: phần cứng, hệ điều hành, phần mềm Web Server, và nội dung của Website.

## Phần cứng của Web Server

Web Server là một máy chủ, có tốc độ xử lý cao, có khả năng lưu trữ nhiều dữ liệu, được bảo mật tốt, luôn luôn ở trạng thái hoạt động.

Theo trang web này http://help.sana-commerce.com/sana-commerce-83/installation/setup-web-and-database-server/hardware-requirements-for-web-and-database-servers thì, yêu cầu về phần cứng của Web Server phụ thuộc vào nhiều yếu tố, ví dụ: lượng người truy cập, kích thước của cơ sở dữ liệu, loại ứng dụng web.

Tuy nhiên, cấu hình phần cứng của Web Server có thể chỉ cần ở mức sau: bộ xử lý 2 x 1,6 GHz, RAM 3.5 GB, đĩa cứng 80GB.

## Hệ điều hành của Web Server

Vì Web Server có thể là một máy chủ, hoặc là một phần mềm, nên có thể sử dụng rất nhiều hệ điều hành khác nhau, từ các hệ điều hành nhúng trong các thiết bị (máy in, router), cho tới các hệ điều hành thuộc các họ hệ điều hành khác nhau (ví dụ: Windows, Unix, Linux).

## Phần mềm Web Server

Có nhiều phần mềm Web Server đang được sử dụng hiện nay, ví dụ: Apache, Nginx, IIS, GWS. Bảng dưới đây là thị phần của các phần mềm này, năm 2016 (nguồn: https://en.wikipedia.org/wiki/Web_server).

- {{< figure src="/images/PhanMemWebServer.PNG" title="PhanMenWebServer">}}

## Nội dung của Website trên Web Server

Nội dung của Website bao gồm toàn bộ tài nguyên giúp cho Website hoạt động. Ví dụ, mã nguồn trang web, hình ảnh, âm thanh, video, cơ sở dữ liệu.


Hình sau là một ví dụ về các thành phần của một Web Server (nguồn: https://en.wikipedia.org/wiki/LAMP_(software_bundle))

### Img

### Lab 5: Tự dựng một web server

### Lab 6: Tìm hiểu về các loại hosting sau? Ưu và nhược điểm của mỗi loại?
## Shared Hosting: 
Shared Hosting được hiểu là một dịch vụ của web hosting nơi mà có rất nhiều website nằm trong một web server được kết nối với internet, bạn có thể hình dung rằng một nhà cung cấp hosting sẽ có một máy chủ đặt trong trung tâm dữ liệu, nhà cung cấp sẽ chia nhỏ các tài nguyên có trong máy chủ để phục vụ người dùng. Nếu website của các bạn không quá nặng thì đây là một sự lựa chọn tuyệt vời cho các bạn vì giá thành của nó khá rẻ so với các dịch vụ khác.

# Đánh giá:
Ưu điểm
Giá thành rẻ hơn khá nhiều so với các dịch vụ khác
Không quá khó khăn để quản lí được dịch vụ này, nó không đòi hỏi bạn phải có quá nhiều kiến thức liên q
uan.
Nhược điểm
Do có giới hạn về dung lượng sử dụng nên cấu hình của nó không được cao
Do có nhiều người cùng sử dụng trên một máy chủ nên dễ bị tấn công cục bộ nếu nó không được bảo mật cao
Nếu tài nguyên của máy chủ phân chia một cách không hợp lí sẽ dẫn đến việc có website chạy nhanh, có website chạy chậm, nếu một website có lượng truy cập lớn thì cá website còn lại sẽ bị chậm.

## VPS Hosting:
VPS là chữ viết tắt của Virtual Private Server – máy chủ ảo cá nhân. VPS hosting là một trong các dịch vụ hosting phổ biến nhất để bạn có thể sử dụng làm nền tảng cho website. Nó dùng công nghệ ảo hóa để tạo tài nguyên riêng trên server cho bạn sử dụng để tách biệt tài nguyên đó khỏi dùng chung với các người dùng khác cùng server vật lý.

Nó an toàn hơn và ổn định hơn so với shared hositng vì bạn không phải chia sẽ không gian lưu trữ với người khác mà được dùng riêng. Và nó cũng rẻ hơn là thuê hẵn một server riêng.

VPS hosting thường được chọn bởi nhiều chủ sở hữu website với lượng truy cập trung bình mà đã vượt giới hạn shared hosting nhưng vẫn chưa cần đến tài nguyên lớn của server riêng.

# Đánh giá:
Ưu điểm
Nhanh và đáng tin cậy hơn server shared hosting.
Vì được đảm bảo về thông số server như bộ nhớ và sức mạnh vi xử lý, bạn sẽ không gặp phải vấn đề tài nguyên bị người khác dùng hết.
Các vấn đề về lượng truy cập đột biến tăng cao không ảnh hưởng đến site của bạn.
Bạn có quyền superuser (root) trên server.
Có độ riêng tư cao hơn, vì files và databases bị khóa khỏi hệ thống server của các người dùng khác.
Dễ dàng nâng cấp. Ngay khi website tăng trưởng, bạn chỉ cần nâng cấp gói hosting để nâng tài nguyên lên mà không phải tốn công chuyển dữ liệu hay chuyển server (RAM, CPU, disk space, bandwidth, etc.).
Nhược điểm
Đặt hơn shared hosting.
Nó cần nhiều kiến thức kỹ thuật để quản lý hơn.
Cấu hình server không đúng có thể tạo ra lỗ hổng bảo mật.

## Cloud Hosting: 
Cloud Hosting là gì ? Cloud Hosting là một thuật ngữ mới ám chỉ dịch vụ Hosting vận hành trên nền công nghệ điện toán đám mây (Cloud computing)

Thực chất về mặt vật lý Cloud Hosting hoạt động tương tự các loại Web Hosting hiện nay, Cloud Hosting cũng sử dụng các control panel quản lý Hosting như DirectAdmin, cũng cấu hình và thiết lập tính năng như Web Hosting tuy nhiên có 1 điểm khác biệt duy nhất giữa Cloud Hosting so với Web Hosting là Cloud Hosting chạy trên các máy chủ Cloud (Cloud Server / Cloud VPS).

Cloud Hosting được hoạt động trên nền công nghệ điện toán đám mây (Cloud computing), sử dụng nền tảng máy chủ tốt nhất của các hãng máy chủ lớn trên thế giới như Cisc cùng với hệ thống lưu trữ Cloud Storage với nguyên tắc lưu trữ phân tán, hoạt động trên hệ điều hành CloudLinux và hơn hết nó sử dụng công nghệ cân bằng tải (Load Balancing) giữa các máy chủ với nhau tạo ra tốc độ truy xuất nhanh hơn nhiều so với các loại Web Hosting thông thường, an toàn, bảo mật dữ liệu cũng cao hơn cũng như giảm tối đa khả năng Downtime cho Website.

Cloud Hosting là gìCloud Hosting hoạt động dựa trên công nghệ tiên tiến nhất trên thế giới hiện nay cho phép không giới hạn số lượng Máy Chủ sử dụng cho một Website hoặc một hệ thống các Website. Cloud Hosting có lợi thế đáng kể so với các giải pháp lưu trữ truyền thống hiện nay như việc sử dụng tài nguyên và bảo mật của một Website lưu trữ trên đám mây luôn được đảm bảo trên nhiều máy chủ thay vì chỉ một như trước đây. Công nghệ điện toán đám mây cũng giúp loại bỏ bất kỳ giới hạn vật lý nào cho sự phát triển và làm cho giải pháp lưu trữ dữ liệu trở nên cực kỳ linh hoạt. Mức độ ổn định của hệ thống Cloud Hosting so với Hosting truyền thống lên tới 300%.

## WordPress Hosting: 
WordPress là một phần mềm mã nguồn mở (miễn phí) được viết bằng ngôn ngữ PHP và hệ quản trị cơ sở dữ liệu MySQL. Phần mềm quản lý nội dung(CMS) mà bạn có thể sử dụng để tạo ra các trang web.
Nói một cách đơn giản đó là một công cụ giúp bạn làm một trang web, blog hoặc tin tức cho riêng bạn. Và đây là một trong những CMS tốt nhất bạn có thể chọn sử dụng để tạo trang web cho riêng mình.
WordPress được phát triển nhằm phục vụ đối tượng người dùng phổ thông. Không cần có quá nhiều kiến thức về lập trình hay website nâng cao. Vì các thao tác trong WordPress rất đơn giản. Giao diện quản trị trực quan, giúp bạn có thể nắm rõ cơ cấu quản lý một website WordPress trong thời gian ngắn.
Nhưng WordPress cũng đủ mạnh và linh hoạt để phục vụ cho những ai đã am hiểu công nghệ.  Hoặc chạy trang web cho việc kinh doanh.
Nếu bạn đang muốn bắt đầu tạo lập một trang Web, hay Blog thì WordPress chính là sự lựa chọn thích hợp.
Đây cũng là sự lựa chọn của hơn 25% trong mười triệu trang web hàng đầu hiện nay. Các trang web nổi tiếng thế giới như: echCrunch, Mashable, CNN, BBC America, Variety, Sony Music, MTV News, Bata, Quartz….

# Đánh giá: 
Ưu điểm:
Chi phí phù hợp hoàn hảo cho các doanh nghiệp vừa và nhỏ.
Thích hợp cho những người mới tạo và quản lý trang web.
Máy chủ chia sẻ không giới hạn ở WordPress.
Plugin vô hạn.
Dễ dàng lắp đặt và tùy biến với cPanel.
Nhược điểm:
Máy chủ chia sẻ có nghĩa là chia sẻ tài nguyên với các trang web khác trên máy chủ đó.  Và tài nguyên được chia sẻ càng lớn thì tốc độ chạy càng chậm.
Bạn có thể có ít hỗ trợ kỹ thuật chuyên biệt hơn. Tuy nhiên, như đã nói ý ở trên, nếu bạn tìm kiếm đúng nhà cung câp. Điều này không phải là một vấn đề.

## Dedicated Hosting: 
Dedicated server là máy chủ chạy trên một chiếc máy tính vật lý, giống như máy bàn nhưng có những thiết bị hỗ trợ đặc biệt như: HDD (hoặc SSD), CPU, RAM, Card mạng, nguồn diện dự phòng. Đồng thời hiện tại đang có hình thức SSD Dedicated server mạnh mẽ được nhiều người ưa chuộng áp dụng từ các đơn vị dịch vụ cho thuê.
Ưu điểm:
– Khách hàng có toàn quyền cài đặt và cấu hình theo nhu cầu. Giống như là Administrator trên chiếc máy để bàn của họ.
Nhược điêm:
– Giá khá cao.

– Khách hàng phải người am hiểu về hệ điều hành tương ứng, cùng nhiều kiến thức về mạng, phần mềm, bảo mật. Họ sẽ phải cài đặt từ A đến Z, ví dụ như: cài Web server, FTP Server, dịch vụ DNS (Domain Name Server), cấu hình nhiều thông số khác nhau. Một người quản trị có tay nghề thấp có thể sẽ dẫn đến nhiều hậu quả nghiêm trọng. Tóm lại họ phải làm tất tần tật mọi thứ và trách nhiệm rất lớn lao.

### Lab 7: 
## Dung lượng lưu trữ (Disk Page):
Là một trong các thông số kỹ thuật quan trọng đối với Web Hosting mà mọi người cần phải biết. Nó đại diện cho khả năng lưu trữ dữ liệu trên Website, nếu dung lượng lưu trữ đã dùng hết, Website sẽ vận hành chậm chạp thậm chí không thể vận hành. Nếu rơi vào trường hợp này tốt hơn hết là người dùng nâng cấp dung lượng lưu trữ.

## Băng thông (Bandwith): 
Băng thông Website là một khái niệm mô tả lượng dữ liệu thông qua Website được phép truyền tải trong một thời gian nhất định (tải lên khi chỉnh sửa, thiết kế mới và đưa dữ liệu vào Web; tải xuống khi người dùng lướt Web và thực hiện các hành vi liên quan đến đọc dữ liệu). Nếu băng thông Web đã gần hết hoặc đã hết thì tốc độ truy cập Website từ người dùng sẽ rất chậm hoặc gần như không thể.

## Cơ chế bảo mật, sao lưu và phục hồi dữ liệu:
Cơ chế bảo mật của server như thế nào (loại máy chủ sử dụng, công nghệ bảo mật đang dùng, cơ chế bảo mật là cứng (thiết bị) hay mềm (soft)…, bên cạnh đó cơ chế sao lưu và phục hồi dữ liệu khi xảy ra sự cố (đối với các máy chủ share Hosting vật lý truyền thống thì vấn đề này là tối quan trọng). Thông dụng và tốt nhất hiện nay là sao lưu 1 tuần/lần được áp dụng tại DIGISTAR, Mắt Bão, PA, Nhân Hòa… cần lưu ý nếu một ngày một lần sao lưu dữ liệu thì vừa tốn kém chi phí mà vừa không bảo mật (một nghịch lý trong ngành lưu trữ máy chủ Hosting).

## Phần mềm hỗ trợ kèm theo:
Thường là các phần mềm quản lý việc tải lên (upload) hoặc tải dữ liệu xuống máy tính người dùng (download), thông dụng là Direct Admin, cPanel, Kloxo nếu là máy chủ Hosting linux còn đối với máy chủ Hosting window là Plesk, Ecompak…

## Tương thích mã nguồn thông dụng:
Các mã nguồn phổ biến có được hỗ trợ không (joomla các phiên bản, wordpress các phiên bản, magento, nukeviet, vbb, xenforo… Tuyệt vời nếu hỗ trợ thêm các phiên bản mã nguồn mới xuất hiện hiện nay như Drupal, Python, Perl…

## Tương thích phiên bản lập trình:
Gói dịch vụ Hosting của nhà cung cấp tương thích với phiên bản lập trình nào (ASP, ASP.NET, PHP 5.1, PHP 5.2, …), cũ hay mới (ví dụ PHP 4x hay 5x, ASP hay ASP.NET…). Và sẽ thật tuyệt vời nếu nhà cung cấp cho phép tùy biến phiên bản lập trình như DIGISTAR.

### Lab 8. Shared hosting miễn phí

### Lab 9. Shared hosting có phí
“Shared hosting trả phí” có nhiều thành phần và dịch vụ để cấu hình hơn so với “shared hosting miễn phí”. Tuy nhiên, cách đưa một website lên hosting thì tương tự.

### Lab 10. Tải và cài đặt Git:
### Img 3 kiểu luôn
- {{< figure src="/images/gitVersion.PNG" title="Git Version">}}
- {{< figure src="/images/gitVersionPS.PNG" title="Git Version PS">}}
- {{< figure src="/images/getVersionGB.PNG" title="Git Version GB">}}
- {{< figure src="/images/gitCommit.PNG" title="Git Commit">}}
- {{< figure src="/images/gitInit&Clone.PNG" title="Git Init n Clone">}}
- {{< figure src="/images/gitPush.PNG" title="Git Push">}}

### Lab 11. Cấu hình môi trường làm việc cho Git:
- {{< figure src="/images/gitconfig.PNG" title="Git Config">}}
### Lab 12. Hiểu về Working Directory, Staging Area và Git Directory:

