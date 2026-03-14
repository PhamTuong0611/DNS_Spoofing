# DNS_Spoofing
1. Mô tả đề tài:
- Đề tài “Tấn công và phòng chống DNS Spoofing trên hệ thống nội bộ” được thực hiện nhằm nghiên cứu cơ chế hoạt động của hệ thống DNS, mô phỏng một cuộc tấn công giả mạo DNS và triển khai giải pháp phòng chống trong môi trường mạng ảo.
- Trong đề tài này, tôi đã xây dựng một môi trường thực nghiệm sử dụng máy ảo để mô phỏng một mạng nội bộ gồm máy tấn công và máy nạn nhân. Máy tấn công sử dụng hệ điều hành Kali Linux để thực hiện tấn công DNS Spoofing thông qua công cụ Ettercap, trong khi máy nạn nhân sử dụng Ubuntu để truy cập website và quan sát kết quả bị chuyển hướng.
- Quá trình thực nghiệm bao gồm việc tạo một trang web giả mạo và cấu hình máy chủ web bằng Apache HTTP Server trên máy tấn công. Sau đó attacker thực hiện tấn công Man-in-the-Middle thông qua kỹ thuật ARP Poisoning và sử dụng DNS Spoofing để thay đổi kết quả phân giải tên miền, khiến máy nạn nhân bị chuyển hướng đến trang web giả mạo do attacker kiểm soát.
- Sau khi mô phỏng thành công cuộc tấn công, đề tài tiếp tục triển khai giải pháp phòng chống bằng cách cấu hình DNSSEC trên hệ thống DNS resolver của máy nạn nhân thông qua dịch vụ Unbound. Việc này giúp xác thực tính toàn vẹn của dữ liệu DNS và ngăn chặn các phản hồi DNS giả mạo từ attacker.
- Kết quả thực nghiệm cho thấy khi chưa triển khai cơ chế bảo mật, máy nạn nhân có thể bị chuyển hướng đến website giả mạo. Tuy nhiên sau khi bật DNSSEC, hệ thống có thể phát hiện và chặn các phản hồi DNS giả mạo, từ đó ngăn chặn thành công cuộc tấn công DNS Spoofing.
2. Thiết lập môi trường
- Máy tấn công sử dụng Kali Linux, cài đặt các công cụ hỗ trợ như Ettercap, Apache Server,... . Máy nạn nhân được giả lập bằng Ubuntu. Và sử dụng phần mềm VMware để thực hiện tấn công.
- Có các card mạng như: VMware Network Adapter VMnet1, VMware Network Adapter VMnet8 và mạng wifi. Các máy ảo sẽ connect với nhau thông qua card mạng VMware Network Adapter VMnet8.
3. Video Demo
- Demo tấn công DNS Spoofing: https://drive.google.com/file/d/1Gm-zRkt16TcfzU4HARK1kVVIgikorlyc/view?usp=sharing
- Demo phòng thủ DNS Spoofing dùng DNSSEC: https://drive.google.com/file/d/1JqmIuuY7H5IMB9o9W09hPWy4zQJR3zBF/view?usp=sharing

