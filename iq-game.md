# IQ GAME Challenge - NightWolf CTF 2023

IQ Game tưởng chừng chỉ là 1 Challenge với những câu hỏi hết sức bình thường :> 

Ở những câu đầu tiên mình vô cùng tự tin, vì chỉ mất đâu đó khoảng 5 giây cho mỗi câu 

<img width="302" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 19 00" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/0e8cf54d-5ed3-46be-bbbe-2a1ac60463c8">

<img width="308" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 19 14" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/172b7c79-3cc3-428c-b9c1-cce16f467de1">

<img width="665" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 19 34" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/30c7115f-4b67-499c-83c7-592482bab4c6">

<img width="676" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 19 51" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/01722834-9699-487e-b692-459a22954d61">

Khoan, dừng khoảng chừng là 2s

Việt Nam mình có vô địch world cup hả ta?

<img width="789" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 21 16" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/b8a4b2db-ccbc-4c9c-b3b3-3a7fbbe41eee">

Hmmm vì chưa vô địch lần nào nên mình submit "0" thì thấy trang bị reload :)) submit thử các số >0 thì bị restart

Rồi khúc này cấn cấn nè :)) theo thói quen thì mình check soucre trước xem BTC có để manh mối nào hong
N
<img width="360" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 26 33" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/3a688c0e-671e-41ee-93a4-806c161f6f04">

Ỏ ỏ ỏ secret.css :> 

<img width="219" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 27 52" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/0b4b0b7b-1274-4778-8428-c924577fc7cf">

Nhưng mà như vậy vẫn chưa đủ, mình phải hash cái gì, hash ra rồi bỏ vô đâu, mà ba cái hash này hay liên quan đến cookie lắm :))

Thử 3-4 lần thì mới phát hiện, mỗi level đều có 1 cookie khác nhau

Hmm ngẫm 5 phút, Hint của BTC là "Ai thông minh hơn học sinh lớp 5? - Học sinh lớp 6"

Mà mình đang bị stop ở level5, submit == 0 thì reload, >0 thì restart

Mà cookie mỗi level mỗi khác, mình đoán level5 thì cookie sẽ là "level5"

Vậy muốn vượt qua level5 lên level6 thì mình cần cookie "level6"

Hash thử "level6" bằng hmac sha 256 vớ8 secret key secret-key: NightWolfCTF

<img width="485" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 40 25" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/786c2acb-3d20-42c2-ac43-d0837d1be57f">

Copy cái vừa hash, thay vào cho cookie của level5

:)) ỦA LÀ Z HOI Ó HỎ

<img width="602" alt="Ảnh chụp Màn hình 2023-11-15 lúc 10 44 44" src="https://github.com/dthkhang/nightwolfctf-writeup/assets/98313915/ef224faf-1db2-466b-b733-0d42fe95c479">







