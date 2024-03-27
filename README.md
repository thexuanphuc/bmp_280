
# Làm quen với BMP280 và Arduino Uno

## Mô tả
Tìm hiểu cách đọc dữ liệu và hiệu chỉnh [BMP280](https://cdn-shop.adafruit.com/datasheets/BST-BMP280-DS001-11.pdf) trực tiếp trong arduino, không thông qua library

## Sơ đồ lắp ghép BMP280 và Arduino Uno
note: VCC 3.3v

|  pin  |  Tên pin  |    Ý nghĩa        | Chân Arduino |
|:-----:|:---------:|:------------------|--------------|
|   0   |    VCC    |  supply pin       |    3.3V      |
|   1   |    GND    |  ground           |     GND      |
|   2   |    SCL    |  I2C clock        |     A5       |
|   3   |    SDA    |  I2C data         |     A4       |
|   4   |    CSB    | SPI / Chip Select |              |
|   5   |    SDO    | SPI address       |              |

![image](https://github.com/thexuanphuc/bmp_280/blob/master/BMP280%20Interface%20with%20Arduino.webp)

## Cách hiệu chỉnh

Trong hàm setup(), lấy trung bình 200 giá trị độ cao làm giá trị ban đầu (AltitudeBarometerStartUp)

Điều chỉnh độ nhạy của cảm biến cho indoor/outdoor (sampling for temperature, pressure, normal mode) thông qua register 0xF4 

Điều chỉnh hệ số cho IIR filter thông qua register 0xF5


## Nguồn liên quan
  + https://github.com/CarbonAeronautics
