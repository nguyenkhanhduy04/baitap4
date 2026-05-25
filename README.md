# Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421

Lớp: 58KTPM

**Bài tập 04:**  
# KHAI THÁC N8N ĐỂ TỰ ĐỘNG ĐĂNG BÀI LÊN WORDPRESS
# 
## deadline : 23h59 ngày 25 tháng 5 năm 2026.

# 1. Cấu hình file docker-compose.yml trên ubuntu:
a. Sử dụng lênh 'nano docker-compose.yml' để edit file docker-compose.yml và cấu hình các dịch vụ
  - Mariadb:
    <img width="491" height="299" alt="image" src="https://github.com/user-attachments/assets/d498b963-41a3-485f-b0ed-326c0d0bf387" />
  - PhPAdmin:
    <img width="495" height="271" alt="image" src="https://github.com/user-attachments/assets/882a064f-2f8f-4e75-84e6-4ef9635da149" />

  - WordPress:
    <img width="491" height="364" alt="image" src="https://github.com/user-attachments/assets/5fa3fe5c-0c05-4a58-98df-13c24bf2812b" />

  - Cấu hình n8n trước khi tạo tunel trên cloudflare để trỏ subdomain về:
    <img width="968" height="219" alt="image" src="https://github.com/user-attachments/assets/7de564ac-399e-4e59-90c9-b4a527dfb8a2" />

  - Cấu hình dịch vụ Cloudflare để các subdomain truy cập được vào các dịch vụ:
    <img width="1482" height="870" alt="image" src="https://github.com/user-attachments/assets/ec503ab6-79f8-4a45-9be3-ac42e4038dc4" />
    + Tạo 3 subdomain:
      <img width="1321" height="804" alt="image" src="https://github.com/user-attachments/assets/984f95c3-d145-49db-8aec-7aaa6e6c40a0" />
      <img width="1277" height="750" alt="image" src="https://github.com/user-attachments/assets/919fb4e2-8fda-4e8c-bce4-da2bcc184969" />
      <img width="1295" height="731" alt="image" src="https://github.com/user-attachments/assets/59210f5e-30e9-4c93-8cf7-865e725465c9" />
    + Cấu hình dịch vụ cloudflare trong docker-compose.yml:
      <img width="1447" height="363" alt="image" src="https://github.com/user-attachments/assets/fcf53fa1-5d26-4d12-8f39-ad682b484d11" />

 - Pull các images bằng lệnh ' docker compose up -d' và kiểm tra trạng thái các dịch vụ bằng lệnh 'docker ps'
   <img width="1464" height="229" alt="image" src="https://github.com/user-attachments/assets/926ade3d-51f4-4ed3-bed3-fe2a104eb79f" />
   <img width="1465" height="274" alt="image" src="https://github.com/user-attachments/assets/acc2ffe0-e33d-4ac1-9f7c-6f2c551ff507" />

# 2. Kiểm tra truy cập các dịch vụ thông qua subdomain:
    <img width="1825" height="967" alt="image" src="https://github.com/user-attachments/assets/ed841d6f-1fa5-466b-aec0-78d89235a687" />
    <img width="1898" height="974" alt="image" src="https://github.com/user-attachments/assets/81bbf5fc-09e5-4b43-85f7-c71f5b8ea496" />
    <img width="1809" height="966" alt="image" src="https://github.com/user-attachments/assets/f6d55711-fe28-48c6-830a-f18af2bff6bf" />
# 3. Tạo bài viết trên WordPress:
  - Giới thiệu bản thân:
    <img width="1318" height="937" alt="image" src="https://github.com/user-attachments/assets/b35df76e-0e04-4e1b-9014-e0fd45fe650d" />
  - Giới thiệu về nhữn kiến thức mà em đã học được ở môn Phát triển ứng dụng với mã nguồn mở:
    <img width="1417" height="937" alt="image" src="https://github.com/user-attachments/assets/18caea61-3c0e-4078-9548-9ba00dfa5878" />

# 4. Cấu hình n8n để bot telegram + gemini + js tự động đăng bài lên WordPress:
  Truy cập sub-domain3 để cấu hình n8n:
    - Tạo tài khoản admin:
      <img width="1635" height="922" alt="image" src="https://github.com/user-attachments/assets/9230f8e1-1acd-4494-957c-5b74a49671ab" />
    - Send me a Licence key:
      <img width="1842" height="933" alt="image" src="https://github.com/user-attachments/assets/aa3b8c56-9cbd-4a8f-94fe-4ec42306b979" />
      <img width="1895" height="971" alt="image" src="https://github.com/user-attachments/assets/52520d20-45ed-4b88-bec9-0af9c4bdb414" />
      <img width="1837" height="915" alt="image" src="https://github.com/user-attachments/assets/ae065eb1-eadd-43d2-b1eb-91059be3f2cc" />
      <img width="1909" height="882" alt="image" src="https://github.com/user-attachments/assets/ada31ff3-feb7-4c88-98b0-7dbbb938af70" />
      <img width="1920" height="913" alt="image" src="https://github.com/user-attachments/assets/4c2f5159-418a-4795-a881-a7d90e392300" />

    - Create workflow:
      + Thêm node Telegram và cấu hình:
<img width="1862" height="849" alt="image" src="https://github.com/user-attachments/assets/c3bd2e7e-c7f0-4e14-b318-2e9570ed8925" />
        <img width="1416" height="842" alt="image" src="https://github.com/user-attachments/assets/cbecc6b3-16d1-4afc-bea9-864e41f3f4a0" />
      <img width="1362" height="735" alt="image" src="https://github.com/user-attachments/assets/9821ef11-03b3-4903-b329-bed36bca21a3" />
    + Nối tiếp node Tele là AI Google Gemini => Message a model:
        <img width="1857" height="844" alt="image" src="https://github.com/user-attachments/assets/4c73a9f2-c8ff-4303-ba65-a89b9f17e777" />
        <img width="1524" height="847" alt="image" src="https://github.com/user-attachments/assets/132ca663-8db8-4c18-bbd8-59fee2b58eab" />
        <img width="1370" height="748" alt="image" src="https://github.com/user-attachments/assets/68cdb087-8cd6-41b2-a5e7-4c1449caccc9" />
        <img width="1863" height="855" alt="image" src="https://github.com/user-attachments/assets/f84ba72a-a381-4a15-b01c-d54567a0bd34" />
        <img width="1854" height="846" alt="image" src="https://github.com/user-attachments/assets/85342a2e-6568-4559-a53d-bed540aa163f" />

    + Nối tiếp là node Code in JavaScript:
  <img width="1850" height="844" alt="image" src="https://github.com/user-attachments/assets/37143568-a5a5-4459-bc84-9cf2c0f30e74" />

    + Add (nối tiếp vào sau node Code in JavaScript) node: WordPress => Create a Post
  <img width="1854" height="826" alt="image" src="https://github.com/user-attachments/assets/175207f6-ac35-4718-be20-143b9c79727f" />
      <img width="1824" height="954" alt="image" src="https://github.com/user-attachments/assets/9a245c4b-7b2f-447d-9535-36dd54141c52" />
      
  
        
      





