# SEI500C LineageOS 22.2 — Android 15

Hướng dẫn cài đặt ROM LineageOS 22.2 (Android 15) cho thiết bị SEI500C.

---

## 🛠 Công cụ cần thiết

Tải **Amlogic USB Burning Tool v2** tại đây:
👉 [Link tải](https://mega.nz/folder/j9F1SKrZ#FhQyNe1LEID-sM1vRrzjFg)

## 📥 Tải ROM mới nhất

Tải **2 file** từ trang Releases bên dưới:

👉 [**Trang Releases**](https://github.com/daivietpda/SEI500C-LineageOS/releases)

| File | Công dụng |
|------|-----------|
| `aml_install_package.img` | Nạp qua USB Burning Tool |
| `lineage-22.2-20260723-UNOFFICIAL-tai.zip` | Cập nhật trong Recovery |

---

## 📖 Hướng dẫn cài đặt chi tiết

### Bước 1: Nạp file IMG qua USB Burning Tool

1. Mở **Amlogic USB Burning Tool v2**.
2. Nhấn **File** → **Import image** → chọn file `aml_install_package.img`.
3. **Quan trọng:** Bỏ chọn hai ô sau:
   - ❌ `Erase Flash`
   - ❌ `Erase Bootloader`
4. Nhấn **Start** trên tool.
5. **Lật ngửa box**, dùng tăm **giữ nút Reset** ở đáy box.
6. **Cắm cáp USB cổng 2.0** vào cổng USB 2.0 trên máy tính, **cắm điện cho box** — **vẫn giữ chặt tăm**.
7. **Đợi khoảng 15 giây** rồi **thả tăm** ra.
8. Tool sẽ tự động nhận thiết bị và bắt đầu nạp. ✅

### Bước 2: Khởi động vào Recovery

1. Sau khi nạp xong, **rút nguồn điện** của SEI500C.
2. **Cắm lại nguồn** — thiết bị sẽ tự động boot vào **Recovery**.

### Bước 3: Cập nhật file ZIP

1. Trong Recovery, chọn **Update** (hoặc **Apply update**).
2. Chọn file **.zip** đã tải về.
3. Xác nhận và chờ quá trình hoàn tất.

### Bước 4: Xoá dữ liệu (Wipe)

1. Vào **Wipe** → chọn **Factory reset / Wipe data**.
2. Xác nhận xoá dữ liệu.

### Bước 5: Khởi động lại

1. Chọn **Reboot system now**.
2. Chờ thiết bị khởi động. Chúc mừng! Bạn đã cài đặt thành công **LineageOS 22.2 (Android 15)**! 🎉

---

## � Changelog

Xem lịch sử thay đổi các phiên bản tại đây:

👉 [**CHANGE-LOG.md**](CHANGE-LOG.md)

---

## �🔗 Nguồn tham khảo (Source code)

- [Device tree — android_device_sei_tai](https://github.com/daivietpda/android_device_sei_tai)
- [Vendor blobs — proprietary_vendor_sei_tai](https://github.com/daivietpda/proprietary_vendor_sei_tai)
- [Kernel — android_kernel_amlogic_linux-4.9](https://github.com/daivietpda/android_kernel_amlogic_linux-4.9)
- [LineageOS](https://github.com/LineageOS/)

---

## 📬 Liên hệ

Telegram: [@daivietpda](http://t.me/daivietpda)
