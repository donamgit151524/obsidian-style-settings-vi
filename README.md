# Style Settings — Việt hóa

Bản tùy chỉnh tiếng Việt dựa trên Style Settings **1.0.9** của mgmeyers, phát hành **1.0.9-vi.1**. Đây không phải bản phát hành chính thức của tác giả gốc.

## Công dụng

Style Settings hiển thị các tùy chọn giao diện mà theme, plugin hoặc đoạn CSS cung cấp: màu sắc, kích thước, khoảng cách, độ đậm và công tắc ẩn/hiện. Bạn có thể chỉnh các tùy chọn này mà không cần sửa mã CSS thủ công.

Plugin không tự tạo tùy chọn cho mọi theme. Theme/plugin phải có khối cấu hình `@settings` trong CSS thì nhóm tương ứng mới xuất hiện.

## Cách dùng với PDF++

1. Cài và bật Style Settings cùng PDF++.
2. Mở **Cài đặt → Style Settings**. Có thể chạy lệnh **Style Settings: Mở khung cài đặt giao diện** để mở một khung riêng.
3. Mở nhóm **PDF++**. Các nhóm tô sáng, vùng chọn chữ nhật, cửa sổ xem trước, thanh công cụ, thanh bên và phím tắt Vim sẽ hiện nếu PDF++ đã nạp cấu hình CSS.
4. Ví dụ: mở **Tô sáng → Độ đậm của màu tô sáng** và kéo thanh trượt để điều chỉnh độ đậm. Dùng **Chiều rộng thanh bên (px)** để chỉnh thanh bên PDF.
5. Dùng nút **Khôi phục mặc định** cạnh từng mục nếu muốn hoàn tác tùy chỉnh của mục đó.

Các thay đổi được lưu vào cấu hình Style Settings trong vault hiện tại. Không làm thay đổi nội dung PDF. Một số tùy chọn CSS chỉ thấy rõ sau khi đóng/mở lại khung PDF.

## Tìm kiếm, xuất và nhập cấu hình

- Ô **Tìm cài đặt giao diện…** tìm theo tên và mô tả; các nhãn PDF++ đã dịch có thể được tìm bằng tiếng Việt.
- **Xuất** tạo JSON cho toàn bộ hoặc nhóm cài đặt; có thể **Sao chép vào bảng tạm** hoặc **Tải xuống**.
- **Nhập** nhận tệp JSON hoặc nội dung JSON được dán vào hộp thoại. Việc nhập có thể ghi đè các giá trị đang dùng; xuất cấu hình hiện tại trước khi nhập cấu hình khác.
- **Khôi phục toàn bộ cài đặt về mặc định** áp dụng cho nhóm tương ứng. Chỉ dùng khi muốn bỏ các tùy chỉnh của nhóm đó.

## Khi không có nhóm cài đặt nào

Kiểm tra theme/plugin đã bật và có hỗ trợ Style Settings. Bản cài không chứa một theme riêng. Các CSS snippet cần được đặt trong `.obsidian/snippets` rồi bật ở phần Giao diện của Obsidian. Với PDF++, thử đóng/mở lại khung cài đặt hoặc tải lại PDF++.

## Cài qua BRAT

Trong **BRAT → Add beta plugin**, nhập:

```text
donamgit151524/obsidian-style-settings-vi
```

Chọn bản mới nhất rồi thêm plugin; bật **Enable after installing the plugin** nếu muốn dùng ngay. ID giữ nguyên `obsidian-style-settings`, nên không cài song song hai bản cùng ID. Dùng BRAT để nhận các bản Việt hóa mới; cập nhật từ danh mục Community plugins có thể thay lại bản gốc.

## Phạm vi Việt hóa

- Giao diện nhập/xuất, tìm kiếm, khôi phục mặc định, bộ chọn màu và lệnh mở khung.
- Thêm locale `vi` cho thông báo giá trị mặc định và lỗi cấu hình.
- Dịch 28 tên/mô tả của cấu hình CSS PDF++ khi Obsidian dùng tiếng Việt.
- Tên sản phẩm Style Settings, PDF++, mã màu, ID, khóa JSON, tên biến CSS và giá trị thực tế giữ nguyên.

Tên/mô tả do theme hoặc plugin khác cung cấp được ưu tiên lấy từ `title.vi` và `description.vi` nếu có; nếu không có trong từ điển, giữ nguyên nội dung tác giả cung cấp. Bản này không tự dịch tùy ý mọi theme bên ngoài.

## Mã nguồn và giấy phép

Nguồn gốc: [community-archive/obsidian-style-settings](https://github.com/community-archive/obsidian-style-settings) (repository gốc của mgmeyers hiện chuyển về đây). Giữ nguyên **GNU GPL v3** trong `LICENSE`.

`source-bundle.zip` chứa mã nguồn upstream đúng bản, bản diff và `patch-tools/` với từ điển, công cụ dịch, kiểm tra cùng Acorn và giấy phép của thư viện. Để tái tạo bản dịch, đặt `apply.cjs`, `vi.json`, `acorn.cjs` cạnh nhau rồi chạy `node apply.cjs /duong-dan/main.js` trên bundle gốc 1.0.9; công cụ tạo bản sao `.original` trước khi xử lý. Khi cập nhật upstream cần rà soát lại ranh giới vá và chạy kiểm tra.

Repository và release không chứa `data.json` hoặc cấu hình cá nhân. Muốn sao lưu tùy chỉnh của bạn, tự sao lưu `data.json` hoặc dùng chức năng **Xuất**.
