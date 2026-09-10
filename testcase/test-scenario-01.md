# Test Scenario 01: Đặt chuyến xe và tạo yêu cầu chuyến đi

## 1. Business Process

### Quy trình đặt chuyến xe

```mermaid
flowchart TD

A[Khách hàng đăng nhập hệ thống]
-->B[Nhập điểm đón, điểm đến và loại xe]

B
-->C{Hệ thống kiểm tra dữ liệu}

C
-- Dữ liệu hợp lệ -->
D[Tạo yêu cầu chuyến xe]

D
-->E[Khởi tạo Trip]

E
-->F[Cập nhật trạng thái SEARCHING_DRIVER]

F
-->G[Chuyển sang quy trình tìm tài xế]

C
-- Dữ liệu không hợp lệ -->
H[Thông báo lỗi nhập liệu]
