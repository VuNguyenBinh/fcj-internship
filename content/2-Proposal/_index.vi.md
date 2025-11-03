---
title: "Đề Xuất Dự Án"
date: 2025-09-11
weight: 2
chapter: false
pre: " <b> 2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Thông tin dưới đây chỉ nhằm mục đích tham khảo. Vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn, bao gồm cả phần cảnh báo này.
{{% /notice %}}

# Dự Án AWS Security Scan  
## Giải pháp tự động hóa CI/CD tích hợp phân tích bảo mật và giám sát an toàn hệ thống

### 1. Tóm tắt điều hành  
**Dự án AWS Security Scan** được thiết kế nhằm tự động hóa quá trình kiểm tra bảo mật trong suốt vòng đời phát triển phần mềm, bằng cách tích hợp các dịch vụ AWS như **CodePipeline**, **CodeBuild**, **CodeGuru Reviewer**, và **AWS Security Hub**.  
Dự án này hướng đến các nhóm DevOps hoặc sinh viên đang nghiên cứu về DevSecOps, giúp họ triển khai pipeline CI/CD có khả năng **phát hiện sớm lỗ hổng bảo mật, cảnh báo tự động, và tạo báo cáo an ninh theo thời gian thực**.

### 2. Tuyên bố vấn đề  
*Thách thức hiện tại*  
Trong nhiều dự án phần mềm, quy trình CI/CD thường chỉ tập trung vào việc build và triển khai mà **thiếu sự kiểm soát bảo mật tự động**. Các lỗ hổng bảo mật thường chỉ được phát hiện sau khi hệ thống đã đi vào hoạt động, gây tốn thời gian và tiềm ẩn rủi ro cao.

*Giải pháp đề xuất*  
Tích hợp quy trình “Security Scan as Code” vào pipeline tự động:
- **CodePipeline** điều phối toàn bộ quy trình build–scan–deploy.  
- **CodeBuild** chạy các công cụ quét mã nguồn và kiểm thử bảo mật.  
- **CodeGuru Reviewer** thực hiện phân tích mã tĩnh để phát hiện lỗi và vi phạm bảo mật.  
- **AWS Security Hub** và **Amazon Detective** tập trung cảnh báo và tổng hợp dữ liệu từ **CloudWatch**, **GuardDuty**, và **CloudTrail**, giúp quản trị viên nhận diện rủi ro trên toàn hệ thống.  

Mọi thay đổi trong mã nguồn đều được quét tự động, và khi phát hiện bất thường, hệ thống sẽ gửi thông báo qua **Amazon SNS**.

### 3. Kiến trúc giải pháp  
Pipeline bao gồm **năm giai đoạn chính**: phát triển, build, quét bảo mật, triển khai và giám sát.

![Kiến trúc dự án AWS Security Scan](/images/2-Proposal/Security%20Scan%20project%20AWS.drawio.png)

*Các dịch vụ AWS được sử dụng:*  
- **GitLab**: Kho lưu trữ mã nguồn, kích hoạt pipeline mỗi khi có commit mới.  
- **AWS CodePipeline**: Tự động hóa toàn bộ quy trình CI/CD.  
- **AWS CodeBuild**: Build ứng dụng và chạy các công cụ kiểm thử bảo mật (ví dụ: SonarQube, Trivy, Bandit).  
- **AWS CodeGuru Reviewer**: Thực hiện đánh giá mã bằng AI, phát hiện lỗi và đề xuất cải tiến.  
- **AWS Security Hub**: Trung tâm quản lý kết quả quét bảo mật và kiểm tra tuân thủ.  
- **Amazon Detective**: Phân tích log và phát hiện các hoạt động đáng ngờ.  
- **Amazon CloudWatch** và **AWS GuardDuty**: Cung cấp giám sát liên tục và phát hiện mối đe dọa.  
- **Amazon SNS**: Gửi cảnh báo khi phát hiện lỗ hổng hoặc hành vi bất thường.  

Kiến trúc này giúp đảm bảo quy trình CI/CD được tích hợp đầy đủ các bước kiểm tra bảo mật tự động, phân tích thông minh, và giám sát tập trung xuyên suốt vòng đời phát triển phần mềm.

### 4. Kết quả mong đợi  
- **Security-first CI/CD Pipeline**: Tích hợp quét và phân tích tự động trong từng lần commit.  
- **Improved Efficiency**: Giảm khối lượng công việc kiểm thử thủ công.  
- **TEnhanced Visibility**: Bảng điều khiển tập trung và cảnh báo thời gian thực giúp nâng cao nhận thức an ninh hệ thống.  
- **Practical Learning Resource**: Là ví dụ điển hình cho việc tự động hóa bảo mật trong DevSecOps sử dụng dịch vụ AWS.  
