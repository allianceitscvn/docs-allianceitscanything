# Cấu hình CI/CD cho SMSF

Đã cài đặt jenkins trên server

Tạo sẵn các thư mục:

* ```
  C:\\publishSMSFLive
  C:\\www\\smsf-live\\api
  C:\\www\\smsf-live\\backup\\
  C:\\www\\smsf-live\\web\\
  C:\\www\\smsf-live\\web-admin\\
  ```

Truy cập jenkins: [http://34.116.0.107/??:9090/](http://34.116.0.107/??:9090/)

Đăng nhập jenkins

Tạo mới job cho API

* Name: Live-SMSF-API
* Type: Pipeline
* Cấu hình:
  * Bật setting để hạn chế việc server phải build cùng lúc quá nhiều
    * Do not allow concurrent builds
    * Throttle builds = 1
    * Trigger builds remotely: key

Tạo mới job cho Web

* Name: Live-SMSF-ReactJS-App
* Type: Pipeline

Tạo mới job cho Web Admin

