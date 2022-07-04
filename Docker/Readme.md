# Bài tập docker

1. Build 1 service php (https://hub.docker.com/_/php), 1 serivce nginx (https://hub.docker.com/_/nginx) để cho thể show được trang php info lên web bằng docker

* Build 1 service nginx

    * Write file Dockerfile
    ![](./images/c1Docker/1nginx.png)

    * Build service nginx
    ![](./images/c1Docker/2nginx.png)

    * Run service
    ![](./images/c1Docker/3nginx.png)

    * Result
    ![](./images/c1Docker/4nginx.png)

* Build 1 service php
    * Write file Dockerfile
    ![](./images/c1Docker/1php.png)

    * Write file index.php
    
    ![](./images/c1Docker/1.2php.png)

    * Build service nginx
    ![](./images/c1Docker/2php.png)

    * Run service
    ![](./images/c1Docker/3php.png)

    * Result
    ![](./images/c1Docker/4php.png)

2. Tổ chức các service trên vào trong 1 file docker-compose.yml

    * Write file Dockerfile in folder nginx
    ![](./images/c2Docker/1compose.png)

    * Write file helloworld.config in folder nginx
    ![](./images/c2Docker/2compose.png)

    * Write file Dockerfile in folder php
    ![](./images/c2Docker/3compose.png)

    * Write file index.php in folder src
    ![](./images/c2Docker/4compose.png)

    * Write file docker-compose.yml
    ![](./images/c2Docker/5compose.png)

    * Build Docker compose
    ![](./images/c2Docker/6compose.png)

    * Run Docker compose
    ![](./images/c2Docker/7compose.png)

    * Result
    ![](./images/c2Docker/8compose.png)


3.  Thêm 1 service mysql (https://hub.docker.com/_/mysql), viết một chương trình php connect đến service mysql

    * Write file Dockerfile in folder nginx
    ![](./images/mysqlDocker/1mysql.png)

    * Write file helloworld.config in folder nginx
    ![](./images/mysqlDocker/2mysql.png)

    * Write file Dockerfile in folder php
    ![](./images/mysqlDocker/3mysql.png)

    * Write file index.php in folder src
    ![](./images/mysqlDocker/4mysql.png)

    * Write file docker-compose.yml
    ![](./images/mysqlDocker/5mysql.png)

    * Build Docker compose
    ![](./images/c2Docker/6compose.png)

    * Run Docker compose
    ![](./images/c2Docker/7compose.png)

    * Result
    ![](./images/mysqlDocker/6mysql.png)



4. Thêm 1 service mailhog (https://hub.docker.com/r/mailhog/mailhog/), tạo một form có thể nhập nhiều email và sau đó submit  những email đã nhập vào 1 table và gửi  1  template mail giới thiệu về bản thân đến những email đó. Dùng mailhog để tổ chức làm server mail để testing

    * Write file Dockerfile in folder php
    ![](./images/mailhog//1mail.png)

    * Write file docker-compose.yml
    ![](./images/mailhog//2mail.png)

    * Write file index.php in folder src
    ![](./images/mailhog//3mail.png)

    * Write file handle.php in folder src
    ![](./images/mailhog//4mail.png)

    * Write file handle.php in folder src
    ![](./images/mailhog//5mail.png)

    * Build Docker compose
    ![](./images/c2Docker/6compose.png)

    * Run Docker compose
    ![](./images/c2Docker/7compose.png)

    * Result
    * Input email need send

    ![](./images/mailhog//6mail.png)

    * List email databases

    ![](./images/mailhog//7mail.png)

    ![](./images/mailhog//11mail.png)

    ![](./images/mailhog//8mail.png)

    ![](./images/mailhog//9mail.png)

    ![](./images/mailhog//10mail.png)