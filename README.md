# Đây là nơi tôi bắt đầu học về git

Command note:
# khởi tạo ở local
    - khởi tạo 1 project mới: `git init`
    - sau khi thêm 1 file vào trong project (chưa add vào workspace git), `git status` sẽ báo rằng file đó chưa được track
    - `git add "..."` để add 1 file cụ thể vào trong workspace, hoặc `git add .` để add tất cả các thay đổi
    - sau khi sử dụng `git add`, cần git commit để chính thức tạo 1 commit đưa thay đổi vào workspace, đồng thời dùng `-m "message"` để mô tả điều mà git commit thực hiện
    - khi này `git status` cho thấy thành công
    - `git log` sẽ log lại các thông tin về author, date, commit trong các lần commit.
    - `git diff` sẽ được thực hiện bây giờ để hiểu usage
         `git diff` sẽ show những thay đổi trong các file được thay đổi so với lần commit gần nhất? [(-) các dòng đã xoá/ (+) các dòng thêm mới] 
         `q` để quit

# làm việc với remote
    - tạo 1 repository, lấy đường dẫn tới repository
    - về local chạy `git remote add origin {link}`
    - `git remote -v` để xác nhận đã set remote thành công chưa
    - `git push -u origin master` push các thay đổi từ local (đã add) lên remote
        sau khi push, sẽ hiển thị tổng quan quá trình push
    - `git pull origin master` để kéo những thay đổi từ remote về 
    123123123
    123123123
# làm việc với nhánh (branch)
    - `git branch` để show các branch trong local
    - `git branch feature/new-button` một ví dụ để tạo 1 branch mới (feature/new-button) tại local
    - `git checkout feature/new-button` để chuyển sang nhánh vừa tạo để làm việc
    - `git merge feature/new-button` để merge nhánh vào main

    => quy trình làm việc
        tạo nhánh, `git branch feature/new-branch`
        `git checkout feature/new-feature`
            -> thay đổi trên nhánh
        `git add ...`,  `git commit -m ...`
            -> commit thay đổi trên nhánh
        `git checkout master (main)` để trở về nhánh chính trc khi merge
        `git merge feature/new-feature`
            -> merge nhánh vào master
        `git push` do đã add và commit bên nhánh r nên có thể push luôn lên remote
            -> push merge lên remote


# quy trình làm việc thực tế
    git clone cả project về và thực hiện thay đổi trên nhánh đó
        -> git switch sang nhánh làm việc
            -> thực hiện làm việc và các thay đổi
                -> git add / git commit
                    -> git push (chỉ push các thay đổi trên nhánh đang làm việc và thực hiện push)