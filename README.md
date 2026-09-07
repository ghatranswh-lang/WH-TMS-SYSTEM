# VAP WMS+TMS — Mockup (bản test độc lập)

File `index.html` trong thư mục này là bản xuất tĩnh (static) của canvas thiết kế
WMS+TMS cho Việt An Pha — y hệt nội dung trên Claude Design, nhưng có thể mở
trực tiếp bằng trình duyệt hoặc host ở bất kỳ đâu (Vercel, GitHub Pages, Netlify...)
mà không cần đăng nhập Claude.

Đây là bản mockup tương tác (click được các nút, điền form, xem thử các luồng),
không có backend thật — toàn bộ dữ liệu là dữ liệu mẫu nằm trong chính file này.

## Cách đưa lên GitHub

Chạy các lệnh sau **trên máy của bạn** (nơi bạn đã đăng nhập GitHub), trong
thư mục chứa `index.html` và `README.md` này:

```bash
git init
git add .
git commit -m "VAP WMS+TMS mockup"
```

Sau đó vào https://github.com/new để tạo một repo trống (đặt tên tuỳ ý,
ví dụ `vap-wms-tms-mockup`), **không** tick "Add README" để tránh xung đột.
GitHub sẽ cho bạn 2 dòng lệnh dạng:

```bash
git remote add origin https://github.com/<ten-cua-ban>/vap-wms-tms-mockup.git
git branch -M main
git push -u origin main
```

## Cách deploy lên Vercel

Sau khi đã có repo trên GitHub:

1. Vào https://vercel.com/new
2. Chọn "Import Git Repository" và chọn repo vừa tạo ở trên
3. Vercel sẽ tự nhận đây là site tĩnh (Framework Preset: "Other") — không cần
   cấu hình Build Command hay Output Directory gì thêm, cứ để mặc định rồi bấm
   "Deploy"
4. Sau ~30 giây bạn sẽ có 1 link dạng `https://vap-wms-tms-mockup.vercel.app`
   để gửi cho bất kỳ ai test, không cần tài khoản Claude

Mỗi lần bạn (hoặc Claude) cập nhật lại `index.html` và `git push` lên GitHub,
Vercel sẽ tự động build lại và cập nhật link — không cần làm lại từ đầu.

## Lưu ý

- File khá nặng (~3.5MB) vì chứa toàn bộ giao diện + dữ liệu mẫu trong 1 file
  duy nhất — vẫn tải bình thường trên web, không vấn đề gì.
- Đây là bản xuất tĩnh, tách rời khỏi canvas gốc trên Claude — sửa trên bản
  Claude sẽ không tự động cập nhật vào đây; cần xuất lại và push lại khi có
  thay đổi mới.
