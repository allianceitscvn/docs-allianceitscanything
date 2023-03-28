# Build app với eas

## Các bước

* Đăng nhập bằng account expo.dev qua câu lệnh: eas login
* Bổ sung đầy đủ các certificate trên expo.dev của app trước
* Tùy việc muốn build gì để gõ câu lệnh cho phù hợp

```
# Build
eas build --profile development --platform android
eas build --profile preview --platform android
eas build --profile adhoc --platform ios
```
