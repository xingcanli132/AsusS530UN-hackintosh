**Cách cài đặt**
1. Tạo bộ cài USB (hỏi chị google) và cài macOS vào máy bạn (có thể dùng Clover | OpenCore không load được bàn phím =))
2. Tải thư mục **OC** và **Boot** và chép vào thư mục EFI của máy
3. Chỉnh sửa lại PlatformInfo trong **config.plist** (tạo mới bằng [https://github.com/corpnewt/GenSMBIOS])
4. Chép VoodooPS2Controller and VoodooI2C, VoodooI2CHID kext từ thư mục /Kexts in /L/E và cài chúng vào /L/E sau đó rebuild cache bằng Hackintool
5. Chỉnh cài đặt UEFI để file Bootx64.efi lên đầu danh sách boot.
6. Khởi động lại máy và thưởng thức!!

**27/05/2020**
- Cập nhật OpenCore, Kexts
- Cập nhật macOS lên bản 10.15.5
- Thêm kext Apple Intel wifi để chạy được card wifi gắn sẵn trong máy.

**03/05/2020**
- Sửa lại hoạt động phím Fn
- Sửa lại lỗi Touchpad không hoạt động ở 1 số máy
- Đưa VoodooI2C và VoodooPS2 vào OpenCore (phải xoá những Kexts này trong /L/E hoặc tắt chúng trong config.plist)
- Tắt giao diện khởi động (OpenCanopy) và âm thanh khởi động (mở lại trong config.plist)

**12/04/2020**
- Thêm GUI khởi động cho OpenCore và âm thanh (tự kích hoạt âm thanh trong config.plist)
- Tối ưu hoá. Loại bỏ 1 số phần không cần thiết
- Chỉnh về chế độ cân bằng điện năng vs hiệu năng
- Sửa lỗi DRM
- Lỗi còn tồn tại: Thỉnh thoảng mất âm thanh sau khi khởi động từ Windows và chuyển sang MacOS (reset máy bằng giữ nút nguồn vài giây để âm thanh hoạt động lại)

**09/04/2020**
- Cập nhật OpenCore lên v0.5.8
- Cập nhật kexts
- Sửa lỗi boot do IGPU sau khi update lên 10.15.4 (sửa hoàn toàn)
- Lỗi còn tồn tại: Thỉnh thoảng mất âm thanh sau khi khởi động từ Windows và chuyển sang MacOS

**02/04/2020**
- Cập nhật kexts
- Sửa lỗi boot do IGPU sau khi update lên 10.15.4 (tạm thời)

**16/03/2020**
- Cập nhật OpenCore v0.5.6
- fix lỗi boot
- lỗi chưa sửa: không load được VoodooPS2Controller and VoodooI2C, VoodooI2CHID kext từ OpenCore (sửa bằng cách Chép VoodooPS2Controller and VoodooI2C, VoodooI2CHID kext từ thư mục /EFI/OC/Kexts và cài chúng vào /L/E sau đó rebuild cache bằng Hackintool )

**21/02/2020**
- Cập nhật kexts
- Thay thế USBInjectAll thành USBMap

**08/02/2020**
- Sửa ACPI để AsusSMC kext hoạt động
- Sửa lỗi đèn nền bàn phím
- Danh sách phím chức năng Fn:
  + F1: Mute
  + F2/F3: Giảm/Tăng âm
  + F4/F5: Giảm/Tăng độ sáng màn hình
  + F6: Bật/Tắt Touchpad
  + F7/F8: Tăng/Giảm đèn nền bàn phím (16 mức độ)
  + F9/F10/F11/F12: Home/End/PgUp/PgDown
  + Fn + phím cách: Play/Pause âm nhạc
  + Fn + Enter : Sleep máy tính (chạy file install_daemon.sh để hoạt động)
  + Fn + Esc: Tắt/Bật màn hình
- Thêm firmware Bluetooth  
- Sửa hoàn toàn lỗi âm thanh
- Cập nhật OpenCore lên 0.5.5
- Cập nhật toàn bộ kext lên phiên bản mới nhất

**06/12/2019**
- Cập nhật OpenCore lên 0.5.4
- Cập nhật các kexts lên phiên bản mới nhất
- Sửa lỗi kernel panic của Whatevergreen 1.3.6

**18/11/2019**
- Ổn định trên macOS 10.15.1
- Ngừng Cập nhật Clover (chuyển hoàn toàn sang OpenCore)
- Cập nhật OC Bootloader
- Cập nhật Kexts
- Sửa lỗi âm thanh
- Loại bỏ kext USB Wifi (dùng file cài trên trang chủ)

**17/09/2019**
- Dùng OpenCore Bootloader làm Bootloader chính
- Cập nhật OC, kexts
- Thêm hướng dẫn cài driver USB Wifi Comfast CF-811AC

**27/08/2019**
- Thêm OpenCore Bootloader (testing)
- Chỉnh sửa lỗi âm thanh
- Fix Minor bugs

**14/06/2019**
- Tải lên toàn bộ dữ liệu
