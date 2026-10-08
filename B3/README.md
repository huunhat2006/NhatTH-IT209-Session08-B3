# Bài 3: Dockerfile 3 dòng đóng gói trang Web HTML tĩnh

## 1. Yêu cầu
Viết tệp Dockerfile siêu ngắn gọn để tự đóng gói một trang HTML tĩnh thành Docker Image. Tạo một trang web cá nhân đơn giản và đóng gói vào Nginx image.

## 2. File được tạo
- `index.html`: Chứa nội dung `<h1>Hello Docker Session 09!</h1>`.
- `Dockerfile`: Chứa 2 câu lệnh để build image từ `nginx:alpine` và copy `index.html` vào container.

## 3. Các lệnh đã chạy để kiểm tra
```bash
# Build image
docker build -t my-html-app:v1 .

# Khởi chạy container
docker run -d -p 8081:80 --name html-app my-html-app:v1

# Kiểm tra nội dung
curl http://localhost:8081
```

## 4. Kết quả
Lệnh `curl` trả về đúng chuỗi `<h1>Hello Docker Session 09!</h1>`.
