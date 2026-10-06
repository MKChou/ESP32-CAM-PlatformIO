# ESP32-CAM 影像串流

用 PlatformIO 開發 ESP32-CAM，連上 WiFi 後用瀏覽器看即時影像。

## 測試影片

[開發板測試影片](https://youtu.be/YFCGYGUP5rA)

## 需求

- 開發板：AI-Thinker ESP32-CAM（OV2640）
- [PlatformIO](https://platformio.org/)
- 2.4 GHz WiFi（ESP32 不支援 5 GHz）

使用 ESP32-S3 系列的板子時，請改用 `platformio.ini` 最下方註解掉的設定，並在 `src/main.cpp` 切換 `CAMERA_MODEL`。

## 使用

1. 複製 WiFi 設定範本並填入帳密。`src/secrets.h` 已列在 `.gitignore`，不會被上傳。

   macOS / Linux：

   ```bash
   cp src/secrets.h.example src/secrets.h
   ```

   Windows PowerShell：

   ```powershell
   Copy-Item src\secrets.h.example src\secrets.h
   ```

2. 編譯燒錄：

   ```bash
   pio run --target upload
   ```

3. 看序列埠印出的 IP，用瀏覽器打開即可。

   ```bash
   pio device monitor
   ```

## 網址

| 路徑 | 內容 |
| --- | --- |
| `/` | 含即時畫面的網頁 |
| `/stream` | MJPEG 即時串流 |

## 授權

MIT License，詳見 [LICENSE](LICENSE)。
