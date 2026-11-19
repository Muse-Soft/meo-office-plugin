# Meo Office: plugin cho Claude Code

Plugin nối Claude Code với các văn phòng của bạn trên Meo Office (https://meo.genalpha.dev): địa chỉ MCP cùng các quy trình mẫu (xử lý email, GitHub, tóm tắt tài liệu, báo cáo tiến độ, đề xuất hành động).

## Cài đặt

Trong Claude Code, chạy lần lượt:

```
/plugin marketplace add Muse-Soft/meo-office-plugin
/plugin install meo-office@meo-office
```

Lần đầu dùng, Claude Code sẽ mở trang đăng nhập Meo Office (OAuth). Mọi hành động ghi hoặc gửi đều chờ bạn duyệt trong Hộp phê duyệt.

Muốn trỏ tới máy chủ khác: đặt biến môi trường `MEO_OFFICE_URL`.

Repo này được sinh tự động từ nguồn của dự án, không sửa tay.
