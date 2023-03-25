# Cấu hình CI/CD cho SMSF

## Chuẩn bị

Đã cài đặt jenkins trên server

Tạo sẵn các thư mục:

* ```
  C:\\publishSMSFLive
  C:\\www\\smsf-live\\api
  C:\\www\\smsf-live\\backup\\
  C:\\www\\smsf-live\\web\\
  C:\\www\\smsf-live\\web-admin\\
  ```

Chuẩn bị sẵn domain, cấu hình sẵn iis, ssl

Chuẩn bị sẵn token để gọi script api khi cấu hình api

## Thực hiện

Truy cập jenkins: [http://34.116.0.107/??:9090/](http://34.116.0.107/??:9090/)

Đăng nhập jenkins

### Tạo mới job cho API

* Name: Live-SMSF-API
* Type: Pipeline
* Cấu hình:
  * Bật setting để hạn chế việc server phải build cùng lúc quá nhiều
    * Do not allow concurrent builds
    * Throttle builds = 1
    * Trigger builds remotely: key
  * Bổ sung script pipleline tương ứng
    * Cần thư mục đầy đủ
    * Cần cấu hình svn, thông tin account svn trong jenkins
    * Cần link domain
    * Cần link chạy script db, token để chạy
    * Cần kiểm tra có config lần đầu hay chưa để khỏi copy config qua
* Chạy thử

### Tạo mới job cho Web

* Name: Live-SMSF-ReactJS-App
* Type: Pipeline
* Cấu hình:
  * Bổ sung script pipeline tương ứng
    * Cần thư mục đầy đủ
    * Cần cấu hình git, địa chỉ git, branch git release, account git trong jenkins
    * Cần link domain
* Chạy thử
* Cần cấu hình config web nếu lần đầu chạy

### Tạo mới job cho Web Admin

Tương tự như Web với thư mục và địa chỉ web khác

## Bổ sung Chat Bot Google để build từ google chat

Chỉnh sửa chat bot Goolge ở project notifyservice

Sau khi chỉnh xong, upload server

Chạy lệnh để reload bot

```
//kiểm tra app đang chạy - chạy lệnh root trước
pm2 list

//show thông tin app tên là app
pm2 show app

//restart app tên là app
pm2 restart app
```
