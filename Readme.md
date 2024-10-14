# …or create a new repository on the command line

## Chức năng: Khởi tạo một Git repository mới trong thư mục hiện tại. Sau khi khởi tạo, Git sẽ theo dõi các thay đổi trong thư mục.
git init

## Chức năng: Cài đặt Git LFS (Large File Storage) để hỗ trợ quản lý các file lớn. Lệnh này chỉ cần chạy một lần trên hệ thống.
git lfs install

## Chức năng: Theo dõi các file có phần mở rộng .pkl bằng Git LFS, điều này giúp quản lý các file lớn như mô hình machine learning.
git lfs track "*.pkl"

## Kiểm tra lại cấu hình của Git: Bạn có thể xác nhận rằng cấu hình của bạn đã được thiết lập đúng cách bằng cách chạy lệnh sau:
git config --global --get core.autocrlf

## Cảnh báo: Nếu bạn nhận được thông báo về sự chuyển đổi CRLF ↔ LF, hãy đảm bảo Git xử lý điều đó một cách nhất quán.
## Khuyến nghị: Chạy lệnh sau để Git tự động xử lý chuyển đổi dòng trên Windows và Unix-based systems.
git config --global core.autocrlf true  # Đối với Windows, điều này đảm bảo Git chuyển đổi dòng chính xác khi commit và checkout

git config --global core.autocrlf input # Dành cho Unix-based systems để chuyển đổi CRLF thành LF khi commit nhưng không thay đổi khi checkout

## Chức năng: Thêm tất cả các file đã thay đổi vào staging area.
git add .

## Lệnh này sẽ thêm tất cả các tệp trong thư mục hiện tại và sửa đổi kiểu kết thúc dòng theo cấu hình core.autocrlf mà bạn đã thiết lập trước đó. Nó sẽ loại bỏ cảnh báo về việc LF sẽ được thay thế bằng CRLF.
git add --renormalize .

## Chức năng: Thực hiện commit các thay đổi đã staged với thông điệp "first commit using git lfs". Đây là bước lưu lại phiên bản mới của dự án.
git commit -m "first commit using git lfs"

## Chức năng: Đổi tên nhánh hiện tại (thường là master) thành main. Điều này tuân theo chuẩn mới của Git, nơi main được dùng làm nhánh chính thay cho master.
git branch -M main

## Chức năng: Liên kết repository Git của bạn với một repository từ xa (remote) trên GitHub có URL là https://github.com/phamthanhlam0201/Notion.git.
git remote add origin https://github.com/phamthanhlam0201/Notion.git

## Chức năng: Push toàn bộ commit từ nhánh main của repository cục bộ lên nhánh main của repository trên GitHub. Thêm cờ -u để thiết lập nhánh origin/main làm mặc định cho lần push sau.
git push -u origin main


# …or push an existing repository from the command line

## Chức năng: Thêm tất cả các file đã thay đổi vào staging area.
git add .

## Lệnh này sẽ thêm tất cả các tệp trong thư mục hiện tại và sửa đổi kiểu kết thúc dòng theo cấu hình core.autocrlf mà bạn đã thiết lập trước đó. Nó sẽ loại bỏ cảnh báo về việc LF sẽ được thay thế bằng CRLF.
git add --renormalize .

## Chức năng: Thực hiện commit các thay đổi đã staged với thông điệp "first commit using git lfs". Đây là bước lưu lại phiên bản mới của dự án.
git commit -m "Update 14/10/2024"

## Chức năng: Đổi tên nhánh hiện tại thành main nếu chưa đổi tên. Lệnh này không bắt buộc nếu nhánh đã có tên main.
git branch -M main

## Chức năng: Liên kết repository Git cục bộ với repository từ xa trên GitHub. Lệnh này chỉ cần chạy một lần nếu repository chưa liên kết với remote.
git remote add origin https://github.com/phamthanhlam0201/Notion.git

## Chức năng: Push tất cả commit từ nhánh main của repository cục bộ lên nhánh main của repository trên GitHub.
git push -u origin main
