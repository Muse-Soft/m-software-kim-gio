# DESIGN.md — Landing page tiệm đồng hồ thủ công Kim Giờ

Mã task: TEC-220 · Epic: TEC-219 · Repo: Muse-Soft/m-software-kim-gio
Phạm vi: 1 landing page giới thiệu tiệm đồng hồ thủ công Kim Giờ.
Quy tắc dữ liệu thật: địa chỉ, số điện thoại và thông tin liên hệ thật để placeholder
`[CẦN BỔ SUNG]`, không bịa số liệu thật. Mọi giá ghi trên trang đều là giá mẫu.

## 1. Bảng màu (mã hex kèm vai trò)

| Mã hex | Vai trò |
|---|---|
| `#F5F0E8` | Nền chính toàn trang (nền kem ấm) |
| `#EAE0CE` | Nền phụ — khối xen kẽ, thẻ, nền trích dẫn |
| `#1C1A17` | Chữ chính (chữ nâu đen), tiêu đề, nền khối tối |
| `#5C5348` | Chữ phụ — mô tả, ghi chú, nhãn nhỏ |
| `#B08D57` | Điểm nhấn vàng đồng — nút chính, link, đường kẻ nhấn, giá nổi bật |
| `#8C6F3F` | Điểm nhấn đậm — trạng thái hover của nút, viền nhấn |
| `#FFFFFF` | Nền ô nhập form, thẻ nổi trên nền kem |
| `#D8CDB8` | Kẻ mảnh, viền thẻ, đường chia khối |

Quy tắc dùng màu: nền sáng chủ đạo, khối tối `#1C1A17` chỉ dùng cho hero
hoặc khối câu chuyện để mặt số và ảnh nổi bật; vàng đồng `#B08D57` chỉ dùng
cho điểm nhấn, không dùng làm nền diện rộng; không dùng màu ngoài bảng này.

## 2. Font chữ

- Font tiêu đề: **Playfair Display**, serif, subset vietnamese.
  H1 hero: 56px / line-height 1.15, weight 600.
  Tiêu đề khối (H2): 36px / line-height 1.25, weight 600.
  Tiêu đề thẻ (H3): 22px / line-height 1.3, weight 600.
- Font nội dung: **Be Vietnam Pro**, sans-serif, subset vietnamese.
  Thân bài: 17px / line-height 1.65, weight 400.
  Chú thích, nhãn nhỏ: 14px / line-height 1.5, weight 400, chữ hoa
  cách chữ (letter-spacing 0.12em) cho nhãn khối.
- Nạp font qua Google Fonts với `display=swap`; luôn khai báo font
  dự phòng: Playfair Display, Georgia, serif; Be Vietnam Pro, system-ui, sans-serif.

## 3. Phong cách tham chiếu (chỉ một)

**Nhiếp ảnh đồng hồ cổ điển kiểu atelier Thụy Sĩ** — ánh sáng studio tối giản,
nền tối làm nổi mặt số, chi tiết máy cơ được chụp cận cảnh sắc nét, không gian
trống nhiều, nhịp chậm, sang trọng mà không phô trương. Không dùng phong cách
thể thao, công nghệ bóng bẩy hay minh họa hoạt hình.

## 4. Quy tắc hình ảnh

- Ảnh là nội dung chính, không phải trang trí phụ: ảnh lớn, khoảng trắng nhiều.
- Tông ảnh: ấm, ánh sáng vàng nhẹ, độ tương phản vừa, nền tối hoặc nền kem
  đồng tông với bảng màu; tránh ảnh lạnh, ảnh rực rỡ nhiều màu.
- Chủ thể: cận cảnh chi tiết máy cơ, bàn tay thợ, mặt số, dây da, kính lúp;
  không dùng ảnh đồng hồ đeo tay thời trang chung chung lệch tông.
- Tỉ lệ khung từng khối:
  - Hero: 16:9, toàn màn hình, ảnh bàn tay thợ đang lắp bộ máy cơ dưới kính lúp.
  - Bộ sưu tập: thẻ 4:5, ảnh lớn từng mẫu đồng hồ.
  - Quy trình chế tác: ảnh minh họa từng bước 3:2.
  - Câu chuyện atelier: ảnh 4:3, kèm ảnh phụ 1:1 nếu cần.
  - Dịch vụ bảo dưỡng: ảnh 3:2.
- Mọi ảnh mẫu phải ghi rõ là ảnh mẫu (alt hoặc chú thích kết thúc bằng
  "(ảnh mẫu)") ngay từ bản đầu tiên; không giả vờ là ảnh thật của tiệm.

## 5. Bố cục và cấu trúc trang (theo thứ tự)

1. **Header dính** (sticky, cao 64px, nền `#F5F0E8`): logo chữ "Kim Giờ",
   menu neo tới các khối, nút "Đặt lịch hẹn" màu vàng đồng `#B08D57`.
2. **Hero toàn màn hình**: ảnh 16:9 bàn tay thợ lắp bộ máy cơ dưới kính lúp,
   tiêu đề lớn, một câu mô tả ngắn, nút "Xem bộ sưu tập".
3. **Bộ sưu tập**: lưới ảnh lớn 4:5 từng mẫu đồng hồ, tên mẫu + giá mẫu
   (ghi rõ "Giá mẫu" ngay dưới giá).
4. **Quy trình chế tác — 4 bước**: tháo máy → lắp ráp → căn chỉnh →
   kiểm tra 48 giờ; mỗi bước ảnh 3:2 + mô tả ngắn.
5. **Câu chuyện atelier**: khối nền tối `#1C1A17`, ảnh 4:3, kể nghề thủ công
   bằng tay, không bịa năm thành lập hay tên thợ thật.
6. **Dịch vụ bảo dưỡng**: danh sách dịch vụ kèm ảnh 3:2, giá (nếu có) là giá mẫu.
7. **Liên hệ / đặt lịch hẹn**: form chỉ làm giao diện (frontend-only,
   không gửi thật): họ tên, số điện thoại, mẫu quan tâm, ngày hẹn mong muốn;
   khi bấm gửi chỉ hiện dòng "Bản demo — form chưa gửi dữ liệu thật.";
   địa chỉ và số điện thoại của tiệm để `[CẦN BỔ SUNG]`.
8. **Footer**: tên tiệm, menu neo, dòng placeholder `[CẦN BỔ SUNG]` cho
   thông tin liên hệ thật, ghi chú ảnh mẫu.

## 6. Hành vi và responsive

- Điểm ngắt mobile: 768px; dưới 768px mọi lưới về 1 cột, hero giữ ảnh
  toàn chiều rộng, chữ H1 giảm còn 36px.
- Header dính trên cả desktop và mobile; menu mobile có nút mở/đóng hoạt động.
- Không cuộn ngang; bảng giá (nếu có) cuộn ngang trong khung riêng khi hẹp.
- Form không gửi dữ liệu thật, không hứa "tiệm sẽ liên hệ xác nhận".

## 7. Kiểm tra đối chiếu (dành cho Dev và QA)

Dev đối chiếu: đủ 8 khối theo thứ tự §5, đủ 8 mã hex đúng vai trò §1,
đủ 2 font đúng cỡ §2, ảnh đúng tỉ lệ và tông §4, form đúng cơ chế §5.7.
QA đối chiếu: sai màu/font chủ đạo, vỡ bố cục, ảnh lệch tông/kém rõ,
thiếu placeholder `[CẦN BỔ SUNG]` ở dữ liệu thật, hoặc form hứa hẹn liên hệ
thật đều là lỗi phải sửa. Thẩm mỹ thị giác chỉ kết luận khi có ảnh chụp
màn hình; không có thì ghi "chưa kiểm thị giác — mới kiểm mức code".
