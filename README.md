# SEI500C LineageOS 22.2 Android 15
## ℹ️ HƯỚNG DẪN
Giống như trên điện thoại , để cài được được rom LineageOS bắt buộc phải unlock bootloader </br>
Trên SEI500C Android 10 để unlock chúng ta phải sử dụng biện pháp ép buộc , nguồn hướng dẫn ở đây [**Forcibly unlocking the bootloader**](https://wiki.lineageos.org/devices/dopinder/install/#forcibly-unlocking-the-bootloader) <br> <br>


***BƯỚC 1** : 
vào chế độ `Burn Mode` bằng cách nhấn giữ  lỗ reset ở đáy box sau đó cắm cáp usb vào cổng 2.0 rồi cắm nguồn điện <br>
đợi 15s thì bỏ tay lỗ reset ra , trên máy tính sẽ nhận Burn Mode <br>
bạn hãy cài đặt [Amlogic USB Burning Tool  v2](https://mega.nz/folder/j9F1SKrZ#FhQyNe1LEID-sM1vRrzjFg) và mở lên để thấy trạng thái kết nối<br>
tải công cụ update cho [**windows tải ở đây**](https://github.com/khadas/utils/tree/master/aml-flash-tool/tools/windows) <br>
***BƯỚC 2** : Mở PowerSell trên windows và gõ <br>
```
./update bulkcmd "setenv lock 10100000"
./update bulkcmd "setenv oemlock unlock"
./update bulkcmd "saveenv"
./update bulkcmd "reboot bootloader"
```
***BƯỚC 3**
tải file [dtb.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/dtb.img) và [dtbo.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/dtbo.img) về và flash qua fastboot.

```
fastboot flash dtb dtb.img
fastboot flash dtbo dtbo.img
```
khởi động lại bootloader
```
fastboot reboot bootloader
```
kiểm tra xem đã unkock bootloader thành công chưa <br>

```
fastboot getvar unlocked
```
kết quả trả về là `unlocked: yes` là ok , nếu `unlocked: no` bạn cần làm lại bước 1 và bước 2 .<br>

***BƯỚC 4**
tải file [recovery.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/recovery.img) , [boot.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/boot.img) , [vbmeta.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/vbmeta.img) , [logo.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/logo.img) , [super_empty.img](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/super_empty.img) , về và nạp qua fastboot
```
fastboot flash recovery recovery.img
fastboot flash boot boot.img
fastboot flash vbmeta vbmeta.img
fastboot flash logo logo.img
fastboot flash super super_empty.img
```
khởi động vào chế độ recovery
```
fastboot boot recovery.img
```
***BƯỚC 5** . Cài đặt LineageOS từ chế độ recovery <br>
bạn có thể sử dụng điều khiển hồng ngoại của fpt/tv360 để điều khiển bên trong recovery<br>
hoặc cắm điều khiển usb 2.4 hoặc bàn phím máy tính.<br>
Trước tiên  Factory reset / Fomart data / factory reset để làm sạch dữ liệu cũ<br>
Tải xuống tệp zip [lineage-22.2-20260606-UNOFFICIAL-tai.zip](https://github.com/daivietpda/SEI500C-LineageOS/releases/download/v1.0/lineage-22.2-20260606-UNOFFICIAL-tai.zip) <br>
Bạn có thể chép vào usb cắm vào cổng usb 3.0 rồi vào mục Apply update > chọn đến usb > chọn file zip và nạp<br>
nếu bạn không có usb stick bạn có thể cài đặt qua adb sideload<br>
cắm cáp vào cổng usb 2.0 , trên recovery vào mục Apply update > ADB Sideload<br>
trên máy tính gõ <br>
```
adb -d sideload /path/to/lineage-22.2-20260606-UNOFFICIAL-tai.zip
```
quá trình cài đặt diễn ra tự động , đợi sau khi thành công thì chọn khởi động lại và thưởng thức Android 15 <br>



## ⬇️ Download ROM mới nhất
[**Download Latest Release**](https://github.com/daivietpda/SEI500C-LineageOS/releases)

## ℹ️Sources:
- https://github.com/daivietpda/android_device_sei_tai
- https://github.com/daivietpda/proprietary_vendor_sei_tai
- https://github.com/daivietpda/android_kernel_amlogic_linux-4.9
- https://github.com/LineageOS/ <br>
##  Contact:
http://t.me/daivietpda
