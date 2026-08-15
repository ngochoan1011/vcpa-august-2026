# VCPA 20.08.2026 — Slide deck

Bài thuyết trình **"Tăng trưởng bằng công nghệ trong kỷ nguyên AI"** — Đỗ Ngọc Hoan, CEO Wizy Corp.
VCPA Monthly Meeting & Networking · 20/08/2026 · Mississauga, ON.

| File | Nội dung |
|---|---|
| [`index.html`](index.html) | Deck 17 slide — một file duy nhất, không phụ thuộc internet |
| [`plan.md`](plan.md) | Sườn nội dung v3 (nguồn của deck) |
| [`filming.md`](filming.md) | Kế hoạch quay phim tại sự kiện |
| [`about_me.md`](about_me.md) | Hồ sơ nền |
| `assets/` | Ảnh & video |

---

## Chạy thử tại máy

```bash
python3 -m http.server 8000
```

Rồi mở http://localhost:8000

> Mở trực tiếp bằng `file://` cũng chạy được, nhưng một số trình duyệt chặn video local — nên dùng http.server khi test video.

---

## Deploy lên Vercel

**Cách 1 — CLI:**

```bash
npx vercel --prod
```

**Cách 2 — Git:** push repo này lên GitHub rồi Import vào Vercel. Không cần chọn framework (Other), không cần build command, output directory để trống.

Deck là static thuần: `index.html` ở thư mục gốc, không build step.

---

## Phím tắt khi trình chiếu

| Phím | Tác dụng |
|---|---|
| `→` `Space` / `←` | Chuyển slide |
| `S` | **Ghi chú diễn giả** (kịch bản + mốc thời gian từng slide) |
| `T` | Chạy / dừng đồng hồ bài nói (mục tiêu **28:30**) |
| `R` | Đặt lại đồng hồ |
| `C` | Đếm ngược **60 giây** — dùng ở slide 6 (bài tập tại chỗ) |
| `O` | Xem toàn bộ slide, bấm để nhảy tới |
| `F` | Toàn màn hình |
| `?` | Bảng phím tắt |

Chạm/bấm nửa trái = lùi, nửa phải = tiến. Có hỗ trợ vuốt trên tablet.
Deep link theo slide: `...vercel.app/#10`

---

## ⚠️ Còn thiếu — cần bổ sung trước sự kiện

| Việc | File | Ghi chú |
|---|---|---|
| **Video demo lễ tân AI** | `assets/demo.mp4` | Slide 13. Chưa có → deck hiện chỗ trống lịch sự. **Burn phụ đề vào video** — loa hội trường không đáng tin |
| **Mã QR trang tài nguyên** | `assets/qr.png` | Slide 17. Chưa có → deck hiện ô trắng ghi "QR" |
| **Số liệu case khách hàng** | `index.html` slide 11–12 | Đang dùng khung **Nghẽn → Hệ thống** (phương án (b) trong plan.md §3.2). Nếu có số thật thì đổi sang khung "Trước → Sau" |
| **Xác minh năm giải nhất quốc gia** | `index.html` slide 9 | Đang ghi **2005**. Bài báo Phú Yên đăng 2015 nhưng nhắc kết quả 2005 — phải xác minh trước khi lên sân khấu |

## 📸 Về ảnh phòng trọ 8m²

`assets/8m2-room-photo.jpg` được **cắt ra từ** ảnh bìa blog (`8m2-room.jpg`) để bỏ dòng chữ tiếng Anh và watermark — deck là tiếng Việt và slide này theo thiết kế là **không chữ**.

Ảnh gốc chỉ **741 × 553 px**. Deck cố ý giới hạn ảnh ở ~64% chiều rộng màn hình để tránh vỡ hạt khi chiếu lớn. **Nếu xin được bản scan gốc từ gia đình hoặc báo Phú Yên, hãy thay file này** — đây là slide quan trọng nhất của cả bài.

---

## In ra PDF

Mở deck → `Cmd/Ctrl + P` → chọn khổ ngang, bỏ header/footer, bật "Background graphics". Mỗi slide một trang.
