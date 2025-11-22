Đây là nơi tôi bắt đầu học về git

Command note:
    - khởi tạo 1 project mới: `git init`
    - sau khi thêm 1 file vào trong project (chưa add vào workspace git), `git status` sẽ báo rằng file đó chưa được track
    - `git add "..."` để add 1 file cụ thể vào trong workspace, hoặc `git add .` để add tất cả các thay đổi
    - sau khi sử dụng `git add`, cần git commit để chính thức tạo 1 commit đưa thay đổi vào workspace, đồng thời dùng `-m "message"` để mô tả điều mà git commit thực hiện
    - khi này `git status` cho thấy thành công
    - `git log` sẽ log lại các thông tin về author, date, commit trong các lần commit

    - `git diff` sẽ được thực hiện bây giờ để hiểu usage
         `git diff` sẽ show những thay đổi trong các file được thay đổi so với lần commit gần nhất? [(-) các dòng đã xoá/ (+) các dòng thêm mới] 
         `q` để quit

    