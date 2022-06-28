# Bài virtual host, server block apache , nginx

1. Cài đặt apache, ngnix

* Cài đặt apache
![Install Apache](./images/phan1/1InstalApache.png)

* Cài đặt ngnix
![Install ngnix](./images/phan1/2InstallNginx.png)


2. Tạo trên máy mình 2 vitrual host để truy cập đến 2 resource web khác nhau bằng apache

* Bước 1: Tạo thư mục để chứa tập tin và dữ liệu của hai trang web
![Create folder contains data of two pages](./images/phan1/3CreateFileForWeb.png)

* Bước 2: Tạo tập tin cấu hình virtual host
    
    * Mở và chỉnh sửa tập tin cấu hình/etc/apache2/sites-available/vidu1.com.conf

    ![Open vidu1.com.conf](./images/phan1/4apache.png)

    ![Edit vidu1.com.conf](./images/phan1/5apache.png)
    
    * Mở và chỉnh sửa tập tin cấu hình/etc/apache2/sites-available/vidu2.com.conf

    ![Open vidu2.com.conf](./images/phan1/6apache.png)

    ![Edit vidu2.com.conf](./images/phan1/7apache.png)

* Bước 3: Bật virtual host để các cấu hình hoạt động va Khởi động lại máy chủ web Apache

    ![Open vitual host](./images/phan1/8apache.png)

* Bước 4: Kiểm tra xem việc tạo virtual host trên Apache
    * Tạo tập tin index.html trong /var/www/vidu1.com/public_html
    ![Index.html for vidu1](./images/phan1/9apache.png)

    * Nội dung file index.html for vidu1 
    ![content index.html for vidu1](./images/phan1/10apache.png)

    * Tạo tập tin index.html trong /var/www/vidu2.com/public_html
    ![Index.html for vidu2](./images/phan1/11apache.png)

    * Nội dung file index.html for vidu2
    ![content index.html for vidu2](./images/phan1/12apache.png)

* Bước 5 : Cuối cùng, trỏ domain về IP của server
    ![domain](./images/phan1/13apache.png)

    Thêm tên miền
    ![add domain](./images/phan1/14apache.png)

* Kết quả 
    * Truy cập vào địa chỉ vidu1.com 
    ![vidu1.com](./images/phan1/15apache.png)

    * Truy cập vào địa chỉ vidu2.com
    ![vidu1.com](./images/phan1/16apache.png)


3. Tương tự như vậy nhưng làm với với nginx Hướng dẫn cấu hình Virtual Hosts trên Nginx

* Bước 1: Tạo thư mục lưu trữ source code cho 2 website

![folder source for web](./images/phan2/1nginx.png)

* Bước 2: Tạo file index.html cho website vinasupport-1.com, đặt nó ở đường dẫn /var/www/vinasupport_1/index.html 

    * Phân quyền truy cập cho file /var/www/vinasupport_1
    ![vinasupport_1 permission](./images/phan2/2nginx.png)

    * Add content for file /var/www/vinasupport_1 

    ![Content for file /var/www/vinasupport_1](./images/phan2/3nginx.png)

    * Phân quyền truy cập cho file /var/www/vinasupport_2
    ![vinasupport_1 permission](./images/phan2/4nginx.png)

    * Add content for file /var/www/vinasupport_2

    ![Content for file /var/www/vinasupport_2](./images/phan2/5nginx.png)

* Bước 3 : Tạo 2 file Virtual Hosts cho 2 domain

    * Access to /etc/nginx/sites-available/vinasupport-1.conf

    ![Access to vinasupport_1.conf](./images/phan2/6nginx.png)

    * Add content for file /etc/nginx/sites-available/vinasupport-1.conf

    ![Content for file /etc/nginx/sites-available/vinasupport.conf](./images/phan2/7nginxNew.png)

    * Access to /etc/nginx/sites-available/vinasupport-2.conf

    ![Access to vinasupport_1.conf](./images/phan2/8nginx.png)

    * Add content for file /etc/nginx/sites-available/vinasupport-2.conf

    ![Content for file /etc/nginx/sites-available/vinasupport.conf](./images/phan2/9nginxNew.png)

* Bước 4 : tạo 2 file symbolic link tới thư mục /etc/nginx/sites-enabled/
![symbolic link](./images/phan2/10nginx.png)

Reload lại service của Nginx Web Server
![reload service](./images/phan2/11nginx.png)

* Bước 5 : Change domain for virtual host

![Domain](./images/phan2/14nginx.png)

* Results

![vinasupport_1](./images/phan2/12nginx.png)

![vinasupport_](./images/phan2/13nginx.png)


4. Làm một vitrual host tại máy em. Khi truy cập vào vào http://demo.com sẽ show ra dòng chữ Hello world trên trang web.

* Bước 1: Create folder demo999, change permission for file and add index.html

![demo999](./images/phan3/1demo.png)

![add index.html for demo](./images/phan3/2demo.png) 

* Bước 2: Create and add config for file demo 

![Access to config for demo](./images/phan3/3demo.png)

![Add config for demo](./images/phan3/4demo.png)

* Bước 3: Create file symbolic link to folder /etc/nginx/sites-enabled/
![symbolic link](./images/phan3/5nginx.png)

* Bước 4 : Change domain for virtual host

![symbolic link](./images/phan3/6nginx.png)

![symbolic link](./images/phan3/7nginx.png)

* Reload server

![reload server](./images/phan3/8nginx.png)

* Result

![demo result](./images/phan3/9nginx.png)

5. Tạo 1 authenticate basic khi vào trang demo.com sẽ bắt nhập username và password. Gợi ý (.htaccess của apache hoặc auth_basic key của nginx)

* Bước 1: Create a file .htpasswd to save username and password into folder
/etc/nginx

![username](./images/phan4/1htpass.png)

* Bước 2: Create password for haposoft

![password](./images/phan4/2htpass.png)

* Show file created 

![file created](./images/phan4/3htpass.png)

* Bước 3: Config accuracy password Nginx 

![Open file need to config](./images/phan4/6htpass.png)

![accuracy password](./images/phan4/4htpass.png)

* Result 

![Request password](./images/phan4/5htpass.png)

6. (Optional) Tạo ssl (htttps) cho web server with nginx.
