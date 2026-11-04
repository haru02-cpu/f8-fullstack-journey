# Chương 16 — Các thuộc tính CSS khác

## Tổng quan

Chương này tập trung vào một số công cụ CSS phục vụ những mục đích khác nhau: tạo bóng, điều khiển tương tác chuột, hòa trộn màu, đánh số tự động, cắt hình và tính toán kích thước.

Các nội dung đã được ghi nhận trong mục lục F8:

- `box-shadow`
- `pointer-events`
- `mix-blend-mode`
- CSS counters
- `clip-path`
- Hàm `calc()`

## Kiến thức chính

### 1. `box-shadow`

`box-shadow` tạo bóng bên ngoài hoặc bên trong hộp của phần tử.

```css
.card {
    box-shadow:
        inset 7px 7px 15px 5px gray,
        7px 7px 15px 5px violet;
}
```

Thứ tự thường dùng:

```text
offset-x | offset-y | blur-radius | spread-radius | color
```

- `inset` chuyển bóng từ bên ngoài vào bên trong phần tử.
- Có thể khai báo nhiều bóng và ngăn cách chúng bằng dấu phẩy.
- `blur-radius` làm mềm bóng; `spread-radius` làm bóng nở ra hoặc co lại. Hai giá trị này không có cùng tác dụng.
- `box-shadow` bám theo hộp chữ nhật của phần tử. Nó khác `filter: drop-shadow()`, vốn có thể bám theo phần nhìn thấy của hình ảnh.

### 2. `pointer-events`

`pointer-events` quyết định phần tử có nhận tương tác từ con trỏ hay không.

```css
.field__label {
    pointer-events: none;
}
```

Với `pointer-events: none`, thao tác chuột hoặc chạm có thể đi xuyên qua phần tử tới phần tử phía dưới. Cách này hữu ích khi một label hoặc lớp trang trí nằm đè lên input.

Điểm dễ nhầm: thuộc tính này không làm phần tử biến mất và không thay thế thuộc tính `disabled`. Một phần tử tương tác vẫn cần HTML và trạng thái bàn phím phù hợp.

### 3. `mix-blend-mode`

`mix-blend-mode` xác định cách màu của phần tử hòa trộn với nền phía sau.

```css
.banner__text {
    color: white;
    mix-blend-mode: difference;
}
```

Với chữ trắng và chế độ `difference`, phần chữ có thể đổi giữa trắng và đen khi đi qua các vùng nền tương phản.

Điểm dễ nhầm: kết quả phụ thuộc vào màu và nội dung phía sau. Thuộc tính này không đơn thuần là đổi màu chữ, giảm `opacity` hoặc áp dụng `filter`.

### 4. CSS counters

CSS counters tạo và hiển thị số thứ tự bằng CSS mà không phải gõ số trực tiếp trong nội dung.

```css
.steps {
    counter-reset: steps;
}

.steps li {
    counter-increment: steps;
}

.steps li::before {
    content: "Bước " counter(steps) ": ";
}
```

- `counter-reset` khởi tạo bộ đếm, mặc định bắt đầu từ `0`.
- `counter-increment` tăng bộ đếm trên mỗi phần tử lặp.
- `counter()` lấy giá trị hiện tại để dùng trong `content`.

Điểm dễ nhầm: nếu đặt `counter-increment` sai cấp, số có thể chỉ tăng một lần hoặc không tăng theo từng mục.

### 5. `clip-path`

`clip-path` chỉ giữ lại vùng nằm bên trong hình cắt.

```css
.shape {
    clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
}
```

Ví dụ trên tạo một tam giác có đỉnh ở giữa cạnh trên và đáy trùng với cạnh dưới.

Mỗi điểm của `polygon()` có dạng `x y`. Điểm `0% 0%` nằm ở góc trên trái; `100% 100%` nằm ở góc dưới phải.

Điểm dễ nhầm: cần đọc từng cặp tọa độ theo thứ tự các đỉnh. `clip-path` thay đổi phần được nhìn thấy nhưng hộp bố cục ban đầu của phần tử vẫn còn.

### 6. Hàm `calc()`

`calc()` cho phép kết hợp các giá trị và đơn vị trong một phép tính CSS.

```css
.panel__bar {
    width: calc(100% - 40px);
    margin: 0 auto;
}
```

Trong một khung rộng `320px`, thanh trên rộng `280px` và còn `20px` ở mỗi bên.

- Viết tên hàm liền nhau: `calc(...)`.
- Toán tử `+` và `-` cần có khoảng trắng ở hai phía.
- `calc()` hữu ích khi kích thước phụ thuộc đồng thời vào phần trăm và một khoảng cố định.

Điểm dễ nhầm: `100% - 40px` là tổng khoảng bị trừ, không phải khoảng trống của riêng từng bên.

## Kết quả thực hành đã được kiểm chứng

Các kết quả dưới đây lấy từ Practice ngày 03/11/2026. Chúng ghi lại đúng mức hỗ trợ tại thời điểm làm bài, không dùng để kết luận đã thành thạo.

| Nội dung | Kết quả đã kiểm tra | Mức hỗ trợ được ghi nhận |
| --- | --- | --- |
| `calc()` | Dùng `width: calc(100% - 40px)` tạo thanh rộng `280px` trong khung `320px`; hai lề đều `20px` | Đạt ngay lượt đầu được kiểm; không có gợi ý sửa code; chưa xác nhận có tra cứu ngoài chat hay không |
| `box-shadow` | Tạo một bóng xám `inset` và một bóng tím bên ngoài trong cùng khai báo | Đạt ngay lượt đầu được kiểm; không có gợi ý sửa code; chưa xác nhận có tra cứu ngoài chat hay không |
| `clip-path` | Cắt hình vuông thành tam giác bằng `polygon(50% 0%, 0% 100%, 100% 100%)` | Đạt sau gợi ý về tọa độ và có tham khảo Clippy |
| CSS counters | Hiển thị “Bước 1/2/3” bằng `counter-reset`, `counter-increment` và `counter()` | Đạt sau khi được nhắc lại ba bước; phần giải thích thuật ngữ được chỉnh thêm |
| `mix-blend-mode` | Dùng `difference` để chữ trắng trên nền đen và đen trên nền trắng | Đạt sau khi được giải thích trực tiếp tác dụng và giá trị cần thử |
| `pointer-events` | Chưa có bài riêng của chương 16 được ghi nhận trong Practice ngày 03/11 | Chưa đủ bằng chứng để ghi kết quả thực hành |

## Trạng thái thư mục

Tại thời điểm rà soát ngày 04/11/2026, thư mục chương 16 chưa có file demo. Vì vậy README này không dẫn tới ví dụ cục bộ chưa tồn tại.

Các bước phù hợp khi học lại:

- Tự giải thích lại tọa độ của một hình `clip-path` khác.
- Viết lại CSS counters mà không nhìn mẫu.
- Thử một trường hợp `mix-blend-mode` với màu nền khác và dự đoán kết quả trước.
- Tạo một ví dụ nhỏ để phân biệt `pointer-events: none` với trạng thái `disabled`.

README ghi lại nội dung và bằng chứng học tập hiện có; không phải xác nhận đã hoàn thành hoặc thành thạo toàn bộ chương.
