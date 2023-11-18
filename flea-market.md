# Flea Market challenge - NightWolf CTF 2023

Ta có đề bài như sau: 

<img width="825" alt="Ảnh chụp Màn hình 2023-11-18 lúc 23 54 09" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/589ffbad-3382-46ef-9640-9f744a785110">

Giải thích cho ai hong hiểu cái đề:
- Mình có 20 đồng
- Flag thì 22 đồng lận
- Mục tiêu là làm sao để kiếm thêm tiền để mua Flag

Ngó cái là biết dạng bài này là Race Condition :> 

Vậy Race Condition là gì?

- Race Condition là lỗi khi 2 hoặc nhiều threads đồng loạt thực hiện 1 hoặc nhiều thao tác trong cùng 1 lúc, mà không có cơ chế kiểm soát nào để đảm bảo các request thao tác được thực hiện theo thứ tự. (Hình bên dưới là 1 ví dụ)

<img width="499" alt="Ảnh chụp Màn hình 2023-11-18 lúc 23 56 30" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/3f7a8113-2dbb-44e3-9ae8-6fdd7395c9bc">

Oki let go 

Bước 1: mua và bán 1 sản phẩm bất kỳ, ở đây mình mua Scooter có Price ($) = 15

Bước 2: túm cái request sell lại :> 

- Vì sao lại túm cái request sell? Vì khi bạn mua Scooter, bạn bị trừ 15$, và ngược lại, bạn được công 15$
  
- Mình sẽ Race cái sell, mục đích là gửi 1 loạt các request sell, lợi dụng nguyên lý của Race Condition để kiếm thêm $
  
Bước 3: ở đây mình dùng Turbo Intruder ngen :> ai hong biết thỉ Google, mình sẽ Race bằng 1 đoạn script như này:

<img width="513" alt="Ảnh chụp Màn hình 2023-11-19 lúc 00 05 08" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/c3592cda-f90a-4dfc-a877-0bbaf2e1b0a9">

 Sau đó thì ?%s ở cái chỗ ID để Race
 
<img width="301" alt="Ảnh chụp Màn hình 2023-11-19 lúc 00 06 43" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/390a8faf-2041-4f54-9bbb-982dd0efcf42">

Rồi oki xong, Attack thôi, xong rồi thì nhớ Reload lại :>

Vậy là được +15$ rồi nè :>

Ở Turbo Intruder, ta có thể thấy 2 Status code là 200 và 302

- 302 là thao tác sell thành công +15$
- 200 là không tìm thấy ID

<img width="1238" alt="Ảnh chụp Màn hình 2023-11-19 lúc 00 13 35" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/8dc4c398-c6a4-4379-8b43-631a9c52051b">

Tức là ta đã bán Scooter 2 lần và được cộng 30$ 

(Ban đầu có 20$, mua Scooter trừ 15$, còn 5$ và bán Scooter 2 lần +30$, tổng ta có 30$)

Giờ thì mua Flag và final hoi :> 

<img width="487" alt="Ảnh chụp Màn hình 2023-11-19 lúc 00 16 26" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/779de791-10f1-4a63-b5dc-f87cc6a551e7">
