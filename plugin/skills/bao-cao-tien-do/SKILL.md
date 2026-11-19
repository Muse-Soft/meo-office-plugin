---
name: bao-cao-tien-do
description: Tóm tắt và báo cáo tiến độ một dự án/office trên Meo Office dựa trên bảng việc và tài liệu. Dùng khi người dùng nói "báo cáo tiến độ", "dự án đang thế nào", "tóm tắt tình hình" hoặc "việc nào đang trễ".
---

# Báo cáo tiến độ

1. `describe_office` để biết các dự án, bảng việc (connection loại board) và nguồn tài liệu của office. Báo cáo cho một dự án thì truyền `project` ở các bước sau; nếu người dùng chưa nói dự án nào mà office có nhiều dự án, hỏi lại.
2. `board_list` lấy các việc; nếu cần, lọc theo `status` hoặc `assignee`. Với việc quan trọng, `board_get` để đọc bình luận.
3. Nếu có tài liệu kế hoạch/biên bản liên quan, `search` rồi `read` để đối chiếu.
4. Trình bày ngắn gọn theo cấu trúc:
   - **Tổng quan** (1-3 câu).
   - **Đang làm / Chờ / Vướng** (gom theo trạng thái, nêu người nhận và mã việc).
   - **Rủi ro hoặc việc có vẻ trễ** (nêu căn cứ, không suy diễn quá mức).
   - **Việc nên làm tiếp**.
5. Mỗi nhận định ghi rõ mã việc hoặc tên tài liệu làm căn cứ. Thiếu dữ liệu thì nói rõ là thiếu.
6. Chỉ đề xuất tạo/sửa việc khi người dùng muốn; khi đó dùng `board_create`/`board_update` và chuyển `approval_url` cho họ.
