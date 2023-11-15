# Lottery! Challenge - NightWolf CTF 2023

Ở challenge Lottery, hay tiếng việt là Xổ số, BTC không giới hạn số lần tạo tài khoản, và mỗi tài khoản được cấp sẵn 20$

Luật chơi đơn giản, nhập 7 số và submit, ăn giờ lụm tiền, thua thì thôi :))

<img width="546" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 48 37" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/98f1c9d3-f43f-4d82-9556-6ad4b5788136">

Check sơ qua các route, BTC cho mình "mua" Flag với giá khuyến mãi cực sock :))

11 con số 9 :))))

<img width="358" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 50 13" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/1dbbc304-9fdf-4296-b20d-cd8b2189d528">

Check soucre thì hong có "secret" gì hết trơn :<

Chơi đi chơi lại gần chục tài khoản, mà tài khoản nào cũng hết sạch tiền, tỉ lệ win thấp quá...

<img width="345" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 52 33" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/38c631cf-23e1-46f9-aade-b008bd8baf22">

# CHECK HINT:

- Hint của BTC cho bài này là: "you can loan money from TypeJuggling88"

Đọc sơ là biết BTC gợi ý về Type Juggling :>

Cho những ai chưa biết, Type Juggling là quá trình tự ý chuyển đổi kiểu dữ liệu của ngôn ngữ lập trình

Ví dụ: Javascript tự ý chuyển đổi kiểu dữ liệu của a từ string sang integer để thực hiện phép so sánh với b, và trong php cũng tương tự
 
<img width="158" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 06 22" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/304ad2b4-9114-45ec-91f2-bda18d2d0f87">

Mọi người có thể Google tìm hiểu về Type Juggling nha, đây là 1 lỗi rất phổ biến thường hay xảy ra

Còn đây là bảng thống kê các lỗi Type Juggling thường gặp với toán tử "=="

<img width="856" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 09 35" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/d9131013-c868-48ea-a37c-1150ab32c874">

Rồi giờ đủ thông tin rồi, bật Hack Mode lên nè :>

Check qua Request và Respone khi thao tác mua vé số ha

<img width="923" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 13 32" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/71031bfa-5565-457e-b8c7-d26c4ce8d4d2">

Theo như data trong bảng trên thì true == true, true == 1, true == "1"

Giờ thì thay 1 thành true thôi :> 

<img width="915" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 23 30" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/cc6c8aac-bc61-4f9b-916e-7cf3aa1b2f07">

Bậy rồi, lỗi gì vậy ta

Ngẫm 5 phút :> ta có thể dùng array trong json, ai hong biết thì google hen

Giờ bỏ hết true vào cặp ngoặc vuông

<img width="897" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 25 19" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/93c10fb6-85e0-4e67-83b6-80d0f75c8c54">

Done :> giờ hong lẽ Buy đến chết :)))


Mình sẽ code tí ảo thuật

Mình cho chạy multi-thread và ngồi xem nó đào tiền thoi

<img width="963" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 35 11" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/7e067eb5-681f-4cfa-91ab-99d019c5a99f">


Nào đủ tiền thì mua Flag ngen :> 

<img width="1123" alt="Ảnh chụp Màn hình 2023-11-15 lúc 11 38 41" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/4951fe6e-2aab-4cc5-9c2b-acfc6cf2cd1c">

Doneeeeeeee





