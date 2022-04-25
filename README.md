# Production-Counter-8051
Extra Project for Microcontroller/Microprocessor Subject

Viết CT đếm sản phẩm hiển thị giá trị lên led 7 đoạn (tối đa 9999), các thông số về sản phẩm được hiển thị lên LCD (ví dụ như tên sản phẩm, số lượng..).
Dùng nguồn xung để giả lập cho tín hiệu xung từ ngõ ra của mạch cảm biến phát hiện sản phẩm. 

Các phím chức năng:
- START (P2.0): Bắt đầu đếm hoặc tiếp tục đếm (nếu như nút PAUSE được nhấn trước đó) khi quét hết chiều dài của 1 sản phẩm.
- PAUSE (P2.1): Dừng đếm (không còn sản phẩm đi qua, hoặc thiết lập cho bộ đếm dừng mặc dù vẫn còn sản phẩm đi qua).
- RESET (P3.2): Đặt bộ đếm về lại ban đầu (nếu trước đó nhấn nút Pause, thì cần phải nhấn nút START mới có thể đếm được sau khi nhấn nút RESET, còn nếu không nhấn nút PAUSE thì không cần nhấn nút START để bắt đầu đếm sau khi nhấn nút RESET).
- MODE (P2.2): Chọn MODE hoạt động cho bộ đếm sau khi đã đếm xong. Sau khi đếm xong, các nút nhấn khác sẽ không ảnh hưởng, nút nhấn MODE sẽ thiết lập lại bộ đếm và yêu cầu người dùng chọn MODE hoạt động.
- SENSOR (P3.4): Giả lập cho tín hiệu xung từ ngõ ra của mạch cảm biến, thời gian nút nhấn SENSOR ở mức 0 chính là thời gian quét sản phẩm.

Ghi chú: 
- Chiều dài sản phẩm bằng thời gian chân P3.4 ở mức 0.
- Sản phẩm phải có độ dài như nhau, chiều dài sản phẩm được điều chỉnh thích hợp trong phần code.
- MODE 1: đếm với số lượng đặt trước, MODE 2: đếm tự do.
- Máy có thể phát hiện 2 sản phẩm nối đuôi nhau đi qua mạch cảm biến phát hiện sản phẩm. Không thể phát hiện 3 sản phẩm trở lên. 

![image](https://user-images.githubusercontent.com/104365389/165110401-6ada0026-038a-49f8-9e79-93f6e88170b0.png)
          Chọn chế độ. 

![image](https://user-images.githubusercontent.com/104365389/165110521-21f12d89-8b8c-4b11-80c9-7e28a6cedfe2.png)
          Nhập số lượng sản phẩm cần đếm cho MODE 1.
          
![image](https://user-images.githubusercontent.com/104365389/165110646-790ddbf8-b076-4dd5-a07e-1300243f3993.png)
          Đã đếm đủ sản phẩm. (Chiều dài sản phẩm được giả định là thời gian chân P3.4 ở mức 0 trong 0,2s)


