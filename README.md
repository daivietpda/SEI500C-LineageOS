# SEI500C-LineageOS
## ℹ️ HƯỚNG DẪN
Giống như trên điện thoại , để cài được được rom LineageOS bắt buộc bạn phải unlock bootloader </br>
Trên SEI500C này để unlock chúng ta phải sử dụng biện pháp ép buộc dùng aml-flash-tool update </br>
Hướng dẫn ở tại đây unlock ở đây [**Forcibly unlocking the bootloader**](https://wiki.lineageos.org/devices/dopinder/install/#forcibly-unlocking-the-bootloader) <br>
công cụ update cho [**windows tải ở đây**](https://github.com/khadas/utils/tree/master/aml-flash-tool/tools/windows) <br>
trên SEI500C sẽ cần thêm 1 dòng `./update bulkcmd "setenv oemlock unlock"`
tất cả các lệnh cần có </br>
 `./update bulkcmd "setenv lock 10100000"`
 <br>
 `./update bulkcmd "setenv oemlock unlock"`
  <br>
 `./update bulkcmd "saveenv"`
  <br>
 `./update bulkcmd "reboot bootloader"`
  <br>
kiểm tra xem đã unkock bootloader thành công chưa
`fastboot getvar unlocked`
<br>
kết quả trả về là `unlocked: yes` là ok , nếu `unlocked: no` bạn cần làm lại bước bên trên .
các bước còn lại giống như hướng dẫn trên trang [**wiki lineageOS**](https://wiki.lineageos.org/devices/dopinder/install/#flashing-the-dtb-and-dtbo-partitions) <br>

## ⬇️ Download các file cần nạp

[**Download Latest Release**](https://github.com/daivietpda/SEI500C-LineageOS/releases)

## ℹ️Sources:
- https://github.com/daivietpda/android_device_sei_tai
- https://github.com/daivietpda/proprietary_vendor_sei_tai
- https://github.com/daivietpda/android_kernel_amlogic_linux-4.9
- https://github.com/LineageOS/
