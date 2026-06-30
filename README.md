# ESP32-CAM 影像串流

用 PlatformIO 開發 ESP32-CAM，連上 WiFi 後用瀏覽器看即時影像。

## 測試影片

[開發板測試影片](https://youtu.be/YFCGYGUP5rA)

## 使用

1. 複製 WiFi 設定範本並填入帳密：

   ```bash
   cp src/secrets.h.example src/secrets.h
   ```

2. 編譯燒錄：

   ```bash
   pio run --target upload
   ```

3. 看序列埠印出的 IP，用瀏覽器打開即可。

   ```bash
   pio device monitor
   ```s