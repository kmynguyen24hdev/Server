# Bài user, group,  file , ssh

1. Tạo ở máy em 3 user user-A, user-B, user-C và 2 group group-A, group-B

* Bước 1: Tạo user-A, user-B, user-C và thiết lập password
![Create user](./images/createUser.png)

*  Bước 2: Tạo 2 group A và B
![Create group](./images/CreateGroup.png)

2. Cho user-A, user-B vào group-1, user-C vào group-2

* Bước 3: Thêm user-A, user-B vào group-A; thêm user-C vào group-B
![Add user into group](./images/AddUserIntoGroup.png)

3. Tạo 1 file example.txt với phân quyền user-A có  read write exec, group-2 chỉ có read và exec. Các user còn lại có thể read.  Thử login vào user-C và sửa đổi file example.txt điều gì sẽ xảy ra?

* Bước 1: Tạo file example.txt
![example.txt](./images/createExample.png)

* Bước 2: Cấp quyền cho file example.txt 
![examplePermission](./images/permissionForFile.png)

* Bước 3: Chuyển quyền sở hữu file example cho user-A
![userApermission](./images/userAPermission.png)

* Bước 4: Phân quyền cho group--B vào file example
![groupB](./images/groupBPermission.png)

* Bước 5: Kiểm tra lại phân quyền của file example.txt
![checkLastest](./images/CheckPermission.png)

** Login vào user C va sửa file
* Bước 1: Đăng nhập user-C và chỉnh sửa file:
![userC login](./images/userC.png)

* Bước 2:Khi truy cập vào file sẽ thấy như hình
![open file](./images/OpenFIle.png)

* Bước 3: Khi thay đổi file sẽ thấy cảnh báo, không thể thay đổi file
![Edit file error](./images/EditFileError.png)

4. Upload 1 file đến VPN thông qua ssh để ở thư mục /home/ubuntu/k10
* Bước 1: Kết nối sever
![Connect to server](./images/connectToServer.png)

* Bước 2: Tạo file text1.txt va Upload file lên server
![Upload file to server](./images/uploadFile.png)

5. Download 1 file từ máy VPN thông qua ssh để ở thư mục /home/ubuntu/k10/download-test.txt
* Bước 1: Kết nối sever
* Bước 2: Download file download-test.txt tu server lưu vào thư mục data
![Download file](./images/downloadFile.png)

6. Config để 2 máy có thể ssh với nhau mà không cần đòi hỏi mật khẩu.
* Bước 1: Cấu hình máy khách tệp cấu hình OpenSSH toàn hệ thống
![Config openssh](./images/sshConfig.png)

* Bước 2: Chỉnh sửa PasswordAuthentication thành no để không cần nhập mật khẩu khi đăng nhập
![Edit PasswordAuthentication](./images/EditPassAuth.png)

* Bước 3: Sử dụng SSH không cần mật khẩu
![Connect by ssh](./images/Connectssh.png)

7. Sử dụng public key và private key để bảo mật connect giữa 2 máy. 

* Bước 1: Kiểm tra xem SSH key cho máy có sẵn chưa
![Check SSH](./images/checkSsh.png)

* Bước 2: Tạo cặp khóa public và private key
![public and private keys](./images/key.png)

* Bước 3: Copy Public Key để kích hoạt SSH without password
![Copy SSH key](./images/coppySSh.png)

* Bước 4: Ket noi ubuntu
![Connect by ssh](./images/Connectssh.png)