# Các phần mềm cần cài đặt
## 1. Cài đặt driver cho mạch esp
Dưới đây là link bộ cài đặt tương ứng cho từng hệ điều hành:
- [Windows](https://github.com/makerhanoi/meo-guide/raw/master/esp8266-drivers/CH341SER_WINDOWS.zip)
- [Mac OS X](https://github.com/makerhanoi/meo-guide/raw/master/esp8266-drivers/CH341SER_MAC-1.4.zip)
- Linux - không cần cài

## 2. Arduino IDE
Chúng ta sẽ sử dụng Arduino IDE để nạp phần mềm cho mạch ESP8266

### 2.a Cài đặt Arduino IDE
Các bạn nên sử dụng phiên bản Arduino 1.8.2 hoặc cao hơn, các bạn có thể tham khảo link hướng dẫn cài đặt tương ứng cho các hệ điều hành ở dưới đây:
- [Windows 10](https://www.arduino.cc/en/Guide/Windows)
- [Mac OS X](https://www.arduino.cc/en/Guide/MacOSX)
- [Linux](https://www.arduino.cc/en/Guide/Linux)

### 2.b Cài đặt thư viện hỗ trợ mạch ESP

Khi sử dụng NodeMCU ESP8266 thì cần cài đặt thư viện tích hợp hỗ trợ cho ESP8266.

#### Bước 1: Thêm đường dẫn để tải các package cho NodeMCU vào Arduino IDE.

1. Khởi động Arduino IDE, từ màn hình chính chọn **File → Preferences**.
2. Thêm đường dẫn bên dưới vào mục **Addition Boards Manager URLs**: http://arduino.esp8266.com/versions/2.3.0/package_esp8266com_index.json
3. Kết quả sau cùng sẽ như ảnh bên dưới

![](https://raw.githubusercontent.com/makerhanoi/meo-guide/master/step1.png "Thêm đường dẫn tải các package cho NodeMCU vào Arduino IDE")

#### Bước 2: Cài đặt Board esp8266

1. Từ giao diện chính của Arduino IDE, chọn **Tools → Board → Board Managers** ...
2. Tại thanh tìm kiếm của hộp thoại **Board Managers** ta nhập vào `esp8266`, chọn Install để tiến hành tải, cài đặt thư viện

![](https://raw.githubusercontent.com/makerhanoi/meo-guide/master/step2.png "Cài đặt board esp8266 vào Arduino IDE")

### 2.c Cài đặt thư viện hỗ trợ cho firmware của mạch ESP

1. Tải file nén chứa các thư viện [tại đây](https://github.com/makerhanoi/meo-guide/raw/master/support-tools/arduino-library.zip)
2. Giải nén các file trong file zip này vào thư mục sau (chọn thư mục tương ứng với hệ điều hành):
- Windows: **C:\Users\<USERNAME>\Documents\Arduino\libraries**
- Mac OS X: **/Users/<USERNAME>/Documents/Arduino/libraries**
- Linux: **/home/<USERNAME>/Arduino/libraries**

## 3. Cài đặt Docker
Bạn sẽ cần cài Docker nếu bạn muốn sử dụng chính máy tính cá nhân của mình để làm server quản lý các mạch esp8266.

Link hướng dẫn cài đặt cho Windows và Mac OS X:

- [Windows](https://docs.docker.com/docker-for-windows/install/)
- [Mac OS X](https://docs.docker.com/docker-for-mac/install/#download-docker-for-mac)

Trong trường hợp các bạn dùng bản Windows thấp hơn Windows 10 hoặc phiên bản Mac OS X của bạn không hỗ trợ thì có thể sự dụng Docker Toolbox [tại đây](https://docs.docker.com/toolbox/overview/#ready-to-get-started)

Các bạn có thể xem hướng dẫn cài đặt Docker cho các bản phân phối của Linux [tại đây](https://www.docker.com/community-edition#/download), ví dụ như:
- [Ubuntu](https://store.docker.com/editions/community/docker-ce-server-ubuntu?tab=description)

Riêng Ubuntu sẽ phải cài riêng docker và docker-compose vì không có bản gộp như bên Windows và Mac OS X, các bạn có thể tìm trên mạng về hướng dẫn cài đặt 2 phần mềm này. Có một cách cài đặt nhanh dành cho Ubuntu tuy nhiên chúng tôi không chắc chắn 100% sẽ hoạt động trên mọi phiên bản khác nhau của Linux (do at your own risk):

```bash
wget -O - https://gist.githubusercontent.com/wdullaer/f1af16bd7e970389bad3/raw/install.sh| bash
```
