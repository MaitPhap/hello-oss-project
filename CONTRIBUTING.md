# Contributing Guide

Cảm ơn bạn đã quan tâm và đóng góp cho dự án! Tài liệu này hướng dẫn cách báo lỗi, gửi Pull Request và đặt tên commit để việc phát triển dự án được thống nhất, dễ theo dõi.

## 1. Cách báo lỗi (Issue)

Trước khi tạo Issue, hãy kiểm tra danh sách Issue hiện có để tránh tạo báo lỗi trùng lặp.

Khi tạo Issue, cần cung cấp:

- **Tiêu đề:** Ngắn gọn, mô tả rõ vấn đề.
- **Mô tả:** Giải thích chi tiết lỗi đã xảy ra.
- **Các bước tái hiện lỗi:** Liệt kê từng bước để người khác có thể kiểm tra lại.
- **Kết quả mong đợi:** Mô tả hệ thống đáng lẽ phải hoạt động như thế nào.
- **Kết quả thực tế:** Mô tả điều thực tế đã xảy ra.
- **Môi trường:** Phiên bản hệ điều hành, ngôn ngữ/framework hoặc phiên bản dự án liên quan.
- **Ảnh chụp màn hình/log:** Đính kèm nếu giúp làm rõ vấn đề.

### Ví dụ

**Tiêu đề:**
`Không thể đăng nhập khi sử dụng mật khẩu hợp lệ`

**Mô tả:**
1. Mở trang đăng nhập.
2. Nhập tài khoản hợp lệ.
3. Nhập mật khẩu chính xác.
4. Nhấn nút **Đăng nhập**.

**Kết quả mong đợi:** Người dùng đăng nhập thành công.

**Kết quả thực tế:** Hệ thống hiển thị thông báo lỗi và không cho đăng nhập.

Không đưa thông tin nhạy cảm như mật khẩu, API key hoặc dữ liệu cá nhân vào Issue.

## 2. Cách gửi Pull Request

Trước khi gửi Pull Request, hãy đảm bảo thay đổi của bạn đã được kiểm tra và không làm hỏng chức năng hiện có.

### Quy trình

1. Fork repository về tài khoản GitHub của bạn nếu cần.
2. Clone repository về máy.
3. Tạo branch mới từ branch chính:

```bash
git checkout main
git pull origin main
git checkout -b feature/ten-tinh-nang
```

4. Thực hiện thay đổi và viết/cập nhật test nếu cần.
5. Kiểm tra dự án trước khi commit.
6. Commit thay đổi theo quy tắc đặt tên commit bên dưới.
7. Push branch lên repository của bạn:

```bash
git push origin feature/ten-tinh-nang
```

8. Tạo Pull Request vào branch `main`.
9. Mô tả rõ:
   - Bạn đã thay đổi những gì.
   - Vì sao cần thay đổi.
   - Issue liên quan, nếu có.
   - Cách kiểm thử.
   - Những ảnh hưởng hoặc thay đổi đáng chú ý.

### Yêu cầu đối với Pull Request

- Chỉ tập trung vào một tính năng hoặc một vấn đề cụ thể.
- Không đưa các thay đổi không liên quan vào cùng một Pull Request.
- Code phải dễ đọc và tuân thủ quy ước của dự án.
- Không commit mật khẩu, API key, file cấu hình chứa thông tin bí mật hoặc file build không cần thiết.
- Pull Request phải được kiểm tra trước khi gửi.
- Contributor cần xử lý các góp ý trong quá trình review.

## 3. Quy tắc đặt tên Commit

Dự án sử dụng quy ước **Conventional Commits** để lịch sử commit rõ ràng và dễ theo dõi.

Cú pháp:

```text
<type>: <mô tả ngắn>
```

Các loại commit thường dùng:

| Type | Ý nghĩa |
|---|---|
| `feat` | Thêm tính năng mới |
| `fix` | Sửa lỗi |
| `docs` | Thay đổi tài liệu |
| `style` | Thay đổi định dạng, không ảnh hưởng logic |
| `refactor` | Cải tổ code, không thêm tính năng hoặc sửa lỗi |
| `test` | Thêm hoặc sửa test |
| `chore` | Công việc bảo trì, cấu hình hoặc công cụ |

### Ví dụ

```text
feat: add admission chatbot interface
fix: fix login validation error
docs: update installation guide
test: add chatbot service tests
refactor: simplify admission service
chore: update CI configuration
```

### Quy tắc

- Viết commit message ngắn gọn, rõ nghĩa.
- Sử dụng động từ mô tả hành động.
- Không viết message quá chung chung như `update`, `fix`, `change`.
- Mỗi commit nên đại diện cho một thay đổi logic rõ ràng.
- Không đưa thông tin bí mật vào commit message.

## 4. Quy trình đóng góp tổng quát

```text
Issue
  ↓
Tạo branch
  ↓
Phát triển / sửa lỗi
  ↓
Test
  ↓
Commit theo quy tắc
  ↓
Push branch
  ↓
Pull Request
  ↓
Code Review
  ↓
Merge
```

Mọi đóng góp đều được hoan nghênh. Cảm ơn bạn đã giúp dự án phát triển tốt hơn!
