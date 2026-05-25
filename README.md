# Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421 <br>

Lớp: 58KTPM<br>

**Bài tập 04:**  <br>
# KHAI THÁC N8N ĐỂ TỰ ĐỘNG ĐĂNG BÀI LÊN WORDPRESS<br>
# 
## deadline : 23h59 ngày 25 tháng 5 năm 2026.<br>

# 1. Cấu hình file docker-compose.yml trên ubuntu:<br>
a. Sử dụng lênh 'nano docker-compose.yml' để edit file docker-compose.yml và cấu hình các dịch vụ<br>
  - Mariadb:<br>
    <img width="491" height="299" alt="image" src="https://github.com/user-attachments/assets/d498b963-41a3-485f-b0ed-326c0d0bf387" /><br>
  - PhPAdmin:<br>
    <img width="495" height="271" alt="image" src="https://github.com/user-attachments/assets/882a064f-2f8f-4e75-84e6-4ef9635da149" /><br>

  - WordPress:<br>
    <img width="491" height="364" alt="image" src="https://github.com/user-attachments/assets/5fa3fe5c-0c05-4a58-98df-13c24bf2812b" /><br>

  - Cấu hình n8n trước khi tạo tunel trên cloudflare để trỏ subdomain về:<br>
    <img width="968" height="219" alt="image" src="https://github.com/user-attachments/assets/7de564ac-399e-4e59-90c9-b4a527dfb8a2" /><br>

  - Cấu hình dịch vụ Cloudflare để các subdomain truy cập được vào các dịch vụ:<br>
    <img width="1482" height="870" alt="image" src="https://github.com/user-attachments/assets/ec503ab6-79f8-4a45-9be3-ac42e4038dc4" /><br>
    + Tạo 3 subdomain:<br>
      <img width="1321" height="804" alt="image" src="https://github.com/user-attachments/assets/984f95c3-d145-49db-8aec-7aaa6e6c40a0" /><br>
      <img width="1277" height="750" alt="image" src="https://github.com/user-attachments/assets/919fb4e2-8fda-4e8c-bce4-da2bcc184969" /><br>
      <img width="1295" height="731" alt="image" src="https://github.com/user-attachments/assets/59210f5e-30e9-4c93-8cf7-865e725465c9" /><br>
    + Cấu hình dịch vụ cloudflare trong docker-compose.yml:<br>
      <img width="1447" height="363" alt="image" src="https://github.com/user-attachments/assets/fcf53fa1-5d26-4d12-8f39-ad682b484d11" /><br>

 - Pull các images bằng lệnh ' docker compose up -d' và kiểm tra trạng thái các dịch vụ bằng lệnh 'docker ps'<br>
   <img width="1464" height="229" alt="image" src="https://github.com/user-attachments/assets/926ade3d-51f4-4ed3-bed3-fe2a104eb79f" /><br>
   <img width="1465" height="274" alt="image" src="https://github.com/user-attachments/assets/acc2ffe0-e33d-4ac1-9f7c-6f2c551ff507" /><br>

# 2. Kiểm tra truy cập các dịch vụ thông qua subdomain:<br>
    <img width="1825" height="967" alt="image" src="https://github.com/user-attachments/assets/ed841d6f-1fa5-466b-aec0-78d89235a687" /><br>
    <img width="1898" height="974" alt="image" src="https://github.com/user-attachments/assets/81bbf5fc-09e5-4b43-85f7-c71f5b8ea496" /><br>
    <img width="1809" height="966" alt="image" src="https://github.com/user-attachments/assets/f6d55711-fe28-48c6-830a-f18af2bff6bf" /><br>
# 3. Tạo bài viết trên WordPress:<br>
  - Giới thiệu bản thân:<br>
    <img width="1318" height="937" alt="image" src="https://github.com/user-attachments/assets/b35df76e-0e04-4e1b-9014-e0fd45fe650d" /><br>
  - Giới thiệu về nhữn kiến thức mà em đã học được ở môn Phát triển ứng dụng với mã nguồn mở:<br>
    <img width="1417" height="937" alt="image" src="https://github.com/user-attachments/assets/18caea61-3c0e-4078-9548-9ba00dfa5878" /><br>

# 4. Cấu hình n8n để bot telegram + gemini + js tự động đăng bài lên WordPress:<br>
  Truy cập sub-domain3 để cấu hình n8n:<br>
    - Tạo tài khoản admin:<br>
      <img width="1635" height="922" alt="image" src="https://github.com/user-attachments/assets/9230f8e1-1acd-4494-957c-5b74a49671ab" /><br>
    - Send me a Licence key:<br>
      <img width="1842" height="933" alt="image" src="https://github.com/user-attachments/assets/aa3b8c56-9cbd-4a8f-94fe-4ec42306b979" /><br>
      <img width="1895" height="971" alt="image" src="https://github.com/user-attachments/assets/52520d20-45ed-4b88-bec9-0af9c4bdb414" /><br>
      <img width="1837" height="915" alt="image" src="https://github.com/user-attachments/assets/ae065eb1-eadd-43d2-b1eb-91059be3f2cc" /><br>
      <img width="1909" height="882" alt="image" src="https://github.com/user-attachments/assets/ada31ff3-feb7-4c88-98b0-7dbbb938af70" /><br>
      <img width="1920" height="913" alt="image" src="https://github.com/user-attachments/assets/4c2f5159-418a-4795-a881-a7d90e392300" /><br>

    - Create workflow:<br>
      + Thêm node Telegram và cấu hình:<br>
<img width="1862" height="849" alt="image" src="https://github.com/user-attachments/assets/c3bd2e7e-c7f0-4e14-b318-2e9570ed8925" /><br>
        <img width="1416" height="842" alt="image" src="https://github.com/user-attachments/assets/cbecc6b3-16d1-4afc-bea9-864e41f3f4a0" /><br>
      <img width="1362" height="735" alt="image" src="https://github.com/user-attachments/assets/9821ef11-03b3-4903-b329-bed36bca21a3" /><br>
    + Nối tiếp node Tele là AI Google Gemini => Message a model:<br>
        <img width="1857" height="844" alt="image" src="https://github.com/user-attachments/assets/4c73a9f2-c8ff-4303-ba65-a89b9f17e777" /><br>
        <img width="1524" height="847" alt="image" src="https://github.com/user-attachments/assets/132ca663-8db8-4c18-bbd8-59fee2b58eab" /><br>
        <img width="1370" height="748" alt="image" src="https://github.com/user-attachments/assets/68cdb087-8cd6-41b2-a5e7-4c1449caccc9" /><br>
        <img width="1863" height="855" alt="image" src="https://github.com/user-attachments/assets/f84ba72a-a381-4a15-b01c-d54567a0bd34" /><br>
        <img width="1854" height="846" alt="image" src="https://github.com/user-attachments/assets/85342a2e-6568-4559-a53d-bed540aa163f" /><br>

    + Nối tiếp là node Code in JavaScript:<br>
  <img width="1850" height="844" alt="image" src="https://github.com/user-attachments/assets/37143568-a5a5-4459-bc84-9cf2c0f30e74" /><br>

    + Add (nối tiếp vào sau node Code in JavaScript) node: WordPress => Create a Post<br>
  <img width="1854" height="826" alt="image" src="https://github.com/user-attachments/assets/175207f6-ac35-4718-be20-143b9c79727f" /><br>
      <img width="1824" height="954" alt="image" src="https://github.com/user-attachments/assets/9a245c4b-7b2f-447d-9535-36dd54141c52" /><br>
      <img width="1916" height="910" alt="image" src="https://github.com/user-attachments/assets/09be7668-1df9-4461-a39a-08c0756a1b0a" /><br>
<img width="1342" height="728" alt="image" src="https://github.com/user-attachments/assets/483c1df3-9a23-4006-a971-2536185f8a84" /><br>
<img width="1858" height="851" alt="image" src="https://github.com/user-attachments/assets/7f379871-16bd-4d03-955d-d43f8dd854d6" /><br>

  + Publish workflow:<br>
    <img width="1634" height="864" alt="image" src="https://github.com/user-attachments/assets/5fea50ce-2340-4be2-80fc-9cf77268975f" /><br>

- Test chat với bot và đăng bài tự động:<br>
  + Wordpress ban đầu:<br>
    <img width="1919" height="903" alt="image" src="https://github.com/user-attachments/assets/7db79ff3-12ad-4e06-a5c9-805c743bd334" /><br>
  + Chat với bot tele:<br>
    <img width="944" height="2046" alt="image" src="https://github.com/user-attachments/assets/18a01ddf-3ce7-474a-92e9-222f387af88a" /><br>

        
  + Refresh lại trang WordPress:<br>
    <img width="1829" height="931" alt="image" src="https://github.com/user-attachments/assets/98d201c4-4479-455e-a966-68dbe7914e28" /><br>

# 5. Nhận xét kết quả đạt được:<br>
Việc sử dụng docker trên ubuntu để cấu hình các dịch vụ, cloudflare để trỏ vào subdomain của cá nhân, cũng như sử dụng n8n giúp xử lí và liên kết dữ liệu. thông qua n8n, chatbot Tele có thể nhận được lệnh --> gửi lệnh đó tới Gemini --> Js xử lí dữ liêu --> đăng bài tự động lên wordpress đã được liên kết tài khoản




