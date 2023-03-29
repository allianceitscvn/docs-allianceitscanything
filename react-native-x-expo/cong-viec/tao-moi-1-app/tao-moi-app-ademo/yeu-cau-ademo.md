# Yêu cầu ADemo

## Yêu cầu

* Tạo mới app, lưu git ở nhánh dev: git@github.com:allianceitscvn/ademo-react-native.git
* Có cấu trúc tương tự app trackntrace23
  * Mọi thông tin riêng của app nằm ở src/apps/ademo
* Có logo, icon: sử dụng logo AllianceITSC
* Có kết nối firebase:&#x20;
  * Tạo mới project firebase tên: MApp-ADemo
    * Android package: app.allianceitsc.ademo
    * iOS bundle: app.allianceitsc.ademo
  * Nhớ share quyền owner project cho htruong@allianceitsc.com
* Có tính năng analytics của firebase
  * Track screen: Splash, Home, Login
* Có tính năng quản lý crash của firebase
* Có màn hình Splash Screen:
  * Hiện logo app, loading, show chừng 5s mới show màn hình bên trong
* Có màn hình Login:
  * Có 2 input: email/password
  * Có nút login
  * Nhấn login để vào màn hình Home (kiểm tra chỉ cần password là z) là vào
* Có màn hình Home:
  * Là màn hình dạng tab, có 2 tab: Home và User
  * màn hình Home: show chữ Welcome ở giữa màn hình
  * màn hình User:&#x20;
    * Có vùng hiện thị avatar giả và email giả
    * Có nút check update để update OTA (App cần có tính năng update OTA)
    * Có nút logout để quay lại màn hình Login
* Liên kết với project trên expo.dev - account htruong@allianceits.com
  * Tên Project phải đúng là ADemo
* Build file apk đầu tiên, chạy đc trên máy thật
* Note lại quá trình làm, thời gian làm
  * Chia ra làm các phần:
    * Chuẩn bị hình ảnh, icon, git, khởi tạo project, liên kết firebase, expo.dev v...
    * Coding các màn hình
    * Build chạy
