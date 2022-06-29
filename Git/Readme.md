# Bài tập về git

1. Ở trên repo hiện tại, git config local username và email
    * Khởi tạo git

    ![init git](./images/1git.png)

    * Git config local username và email

    ![git conf](./images/2git.png)

2. Checkout master 1 branch là develop

    * Tạo branch develop

    ![develop branch](./images/3git.png)

3. Trên branch develop tạo 1 file demo.log, 1 file index.html với nội dung in ra dòng chữ “Hello world”. Làm thế nào để git không tracking tất cả file .log (dùng .gitignore). Sau đó tạo 1 commit add file index.html

    * Tạo tập tin index.html và demo.log
    
    ![index.html demo.log](./images/4git.png)

    ![index.html content](./images/5git.png)
    
    * Tạo file .gitignore

    ![.gitignore](./images/6git.png)

    ![.gitignore content](./images/7git.png)  
 
    * Commit file vừa tạo
    
    ![git add ](./images/8git.png)

    ![git commit](./images/9git.png)

4. Sửa đổi nội dung trên file index.html sau đó làm thế nào để revert lại file index.html trước khi sửa đổi không dùng undo mà dùng lệnh git.

    * Sửa đổi nội dung file index.html

    ![index.html change](./images/10git.png)

    * Commit file index.html

    ![index.html change](./images/11git.png)

    * Trạng thái hiện tại

    ![log](./images/12git.png)

    * Revert file 

    ![revert file](./images/13git.png)

    * revert thành công và kết quả
    
    ![revert thành công](./images/14git.png)

    ![revert result](./images/15git.png)

5. Tạo 1 file demo.html với nội dung in ra dòng chưa “This is file demo”, tạo một commit mới add file demo.html và push code lên origin.

    * Tạo 1 file demo.html với nội dung in ra dòng chưa “This is file demo”

    ![demo.html](./images/16git.png)

    * commit file demo.html 

    ![demo.html](./images/17git.png)

    * Kết nối remote
    ![git remote](./images/18git.png)

    * push code lên origin

    ![git push origin](./images/19git.png)

    * Result

    ![result origin](./images/20git.png)

6. Sửa đổi lại nội dung file demo.html với nội dung “This is a demo file” như không tạo thêm một commit mới nào cả chỉ là thay thế commit cũ và push lại code lên origin
    
    * Thay đổi file demo.html

    * Kiểm tra trạng thái hiện tại

    * Add file demo.html và commit vào commit cũ

    ![commit amend](./images/21git.png)

7. Tạo 1 branch mới là feature_a, rồi thêm môt file feature.html với nội dung bất kì rồi tạo một commit. Sử dụng git cherry-pick để lấy commit mới của feature_a vào branch develop. 

    * Tạo branch feature_a 

    ![feature_a branch ](./images/23git.png)

    * Tạo file feature.html, add và commit file

    ![feature.html](./images/24git.png)

    * Chuyển sang branch develop cherry-pick feature_a

    (Vì hiện tại feature_a chỉ có 1 commit nên lấy luôn commit hiện có của feature_a)

    lấy commit cụ thể thì gắn hash sau cherry-pick

    ![cherry-pick](./images/25git.png)

    * Kiểm tra

    ![check](./images/26git.png)

8. Sửa đổi file feature.html sau khi cherry-pick ở trên branch develop rồi tạo 1 commit. Sử dụng git rebase branch feature_a với branch develop (Nếu có conflict thì resolve và rebase --continue) 

    * Sửa đổi file feature.html và commit

    ![feature.html change](./images/27git.png)

    * Xóa merge trước đó và chuyển sang branch feature_a

    ~[Del merge pre](./images/28git.png)

    * rebase branch develop và bị conflict 

    ![rebase branch](./images/29git.png)

    * Sửa đổi file conflict và rebase lại

    ![rebase branch](./images/30git.png)
