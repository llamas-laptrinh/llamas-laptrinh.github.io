# llamas-laptrinh.github.io

Trang chủ của app **Nhipo** (Google Play: `com.dtddev.dailyroutine`) và file `app-ads.txt` cho AdMob. Trang tĩnh thuần HTML/CSS, không cần build.

| Đường dẫn | Nội dung |
| --- | --- |
| `/` | Trang chủ tiếng Việt (`index.html`) |
| `/en/` | Trang chủ tiếng Anh (`en/index.html`) |
| `/app-ads.txt` | Khai báo nhà bán quảng cáo cho AdMob |

## app-ads.txt

Publisher ID lấy từ `androidAppId` trong `app.json` của app (phần `pub-…`, bỏ `ca-app-` và `~…`). File phải nằm ở **gốc tên miền**, nên repo này phải tên đúng `llamas-laptrinh.github.io`. Repo project (`…github.io/<tên-repo>/`) không dùng được.

Kiểm tra sau khi deploy:

```bash
curl -i https://llamas-laptrinh.github.io/app-ads.txt   # phải trả 200, text/plain, đúng một dòng google.com, pub-…
```

## Cập nhật nội dung

- Ảnh lấy từ `store/google-play/` của repo app: ảnh chụp màn hình được đổi sang JPEG rộng 540px (`assets/shots/<vi|en>/`), ảnh hero là phần màn hình cắt từ ảnh 1, `og-*.jpg` là feature graphic.
- Màu và font (Plus Jakarta Sans) khớp với `src/theme/theme.ts` của app. Trang tự đổi sang giao diện tối theo cài đặt của máy.
- Nếu đổi sang tên miền riêng: sửa `canonical`, `hreflang`, `og:url`, `og:image` trong cả hai file HTML, và cập nhật ô Website trong Play Console.
