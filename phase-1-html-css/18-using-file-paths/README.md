# Tổng kết sử dụng đường dẫn

## Tương đối / tuyệt đối

- Relative: ./, ../
- Absolute:
    - /
    - https://fullstack.edu.vn
    - //fullstack.edu.vn

---

## Khi nào dùng tương đối / tuyệt đối

### Tương đối

- Gửi source code cho người khác
- Deploy trong subfolder
- Các trường hợp khác

### Tuyệt đối

- Trang được deploy từ root (không trong subfolder)
    - Xác định đi tới cụ thể một tài nguyên
        - https://fullstack.edu.vn
        - https://fullstack.edu.vn/courses/monkey.jpg
    - Từ bất cứ cấp nào muốn đi từ root
        - File có thể bị thay đổi cấp độ
        - Đi về trang chủ. VD: click vào logo ở bất cứ đâu
