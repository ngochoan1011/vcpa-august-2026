# VCPA 20.08.2026 — Slide deck

Bài thuyết trình **"Tăng trưởng bằng công nghệ trong kỷ nguyên AI"** — Đỗ Ngọc Hoan, CEO Wizy Corp.
VCPA Monthly Meeting & Networking · 20/08/2026 · Mississauga, ON.

| File | Nội dung |
|---|---|
| [`index.html`](index.html) | Deck 18 slide — một file duy nhất, không phụ thuộc internet |
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
| `→` `↓` `Space` `PageDown` / `←` `↑` `PageUp` | Chuyển slide — nhận cả **remote trình chiếu** |
| `B` | Màn hình đen — khi muốn khán giả nhìn mình, không nhìn slide |
| `S` | **Ghi chú diễn giả** (kịch bản + mốc thời gian từng slide) |
| `T` | Chạy / dừng đồng hồ bài nói (mục tiêu **28:30**) |
| `R` | Đặt lại đồng hồ |
| `C` | Đếm ngược **60 giây** — dùng ở slide 7 (bài tập tại chỗ) |
| `O` | Xem toàn bộ slide, bấm để nhảy tới |
| `F` | Toàn màn hình |
| `?` | Bảng phím tắt |

Chạm/bấm nửa trái = lùi, nửa phải = tiến. Có hỗ trợ vuốt trên tablet.
Deep link theo slide: `...vercel.app/#10`

---

## ⚠️ Còn thiếu — cần bổ sung trước sự kiện

| Việc | File | Ghi chú |
|---|---|---|
| **Video demo lễ tân AI** | `assets/demo.mp4` | Slide 14. Chưa có → deck hiện chỗ trống lịch sự. **Burn phụ đề vào video** — loa hội trường không đáng tin |
| **Mã QR trang tài nguyên** | `assets/qr.png` | Slide 18. Chưa có → deck hiện ô trắng ghi "QR" |
| **Số liệu case khách hàng** | `index.html` slide 12–13 | Đang dùng khung **Nghẽn → Hệ thống** (phương án (b) trong plan.md §3.2). Nếu có số thật thì đổi sang khung "Trước → Sau" |
| **Xác minh năm giải nhất quốc gia** | `index.html` slide 10 | Đang ghi **2005**. Bài báo Phú Yên đăng 2015 nhưng nhắc kết quả 2005 — phải xác minh trước khi lên sân khấu |

## 📸 Về ảnh phòng trọ 8m² (slide 8)

Deck đang dùng **`assets/060415-DNH.jpg`** — file gốc từ báo Phú Yên, **216 × 162 px**.

Vì ảnh rất nhỏ, slide cố ý trình bày nó **nhỏ như một tấm ảnh cũ ghim trên tường tối** (khung polaroid, rộng 430px, hơi nghiêng) thay vì phóng to full màn hình. **Nhỏ mà sắc tốt hơn to mà nhoè** — và một tấm ảnh cũ nhỏ giữa khán phòng tối cũng đúng tinh thần câu chuyện hơn.

**Các bản khác của cùng tấm ảnh này** (giữ lại để chọn thay thế):

| File | Kích thước | Ghi chú |
|---|---|---|
| `060415-DNH.jpg` | 216 × 162 | **đang dùng** — gốc từ báo Phú Yên |
| `8m2-room-photo.jpg` | 741 × 553 | cùng ảnh, **nhiều pixel hơn 3.4×** — cắt ra từ ảnh bìa blog |
| `8m2-room-photo@2x.jpg` | 1482 × 1106 | bản trên upscale Lanczos 2× |
| `8m2-room.jpg` | 1080 × 1080 | ảnh bìa blog gốc (có chữ tiếng Anh + watermark) |

> 💡 Nếu muốn chiếu ảnh **to hơn**, đổi `src` ở slide 8 sang `assets/8m2-room-photo.jpg` và bỏ class `photo-frame`.
>
> Tốt nhất vẫn là **xin bản scan gốc từ gia đình hoặc toà soạn báo Phú Yên** — đây là slide quan trọng nhất của cả bài.

## 👤 Avatar slide 1

`assets/hoan-avatar.png` (512 × 512) được tạo từ `assets/hoan-do-avatar-final.png`: xoá nền trắng bằng flood-fill từ viền (không đụng vào áo sơ mi sáng màu), cắt vuông quanh đầu, ghép lên đĩa tròn navy rồi cắt tròn + viền gold.

Muốn đổi ảnh khác: thay `assets/hoan-avatar.png` bằng một ảnh **vuông** đã cắt tròn sẵn — không cần sửa CSS.

---

## In ra PDF

Mở deck → `Cmd/Ctrl + P` → chọn khổ ngang, bỏ header/footer, bật "Background graphics". Mỗi slide một trang.
