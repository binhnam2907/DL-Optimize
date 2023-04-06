Link GG Drive để thực nghiệm trên colab : https://drive.google.com/drive/folders/186KaX1MP9tbH2mRg5eyY9GtYLS8VpRNu?usp=sharing

### Overview
- Activation functions (Hàm kích hoạt) và Initializers (tạm dịch: Hàm khởi tạo trọng số) là hai trong số các thành phần xử lý chính trong một mạng Multilayer perceptron (MLP) và có ảnh hưởng rất lớn đến hiệu năng của toàn bộ mô hình trong quá trình huấn luyện.
- Activation functions là các hàm có chức năng chính dùng để chuyển đổi giá trị tuyến tính đầu vào z về một miền giá trị nào đó. Ví dụ, hàm sigmoid(z) có thể đưa giá trị z bất kì về miền giá trị thuộc khoảng (0, 1). Về mặt ý nghĩa, hàm kích hoạt tạo giá trị phi tuyến cho mô hình, giúp mô hình có thể dự đoán được trên các dữ liệu phức tạp hơn (không tuyến tính).

![image](https://user-images.githubusercontent.com/87894596/230276952-7d946c92-714a-453a-87a2-924e6afbeff3.png)

Minh họa về Activation function sử dụng hàm sigmoid

- Initializers là các hàm trong thư viện tensorflow dùng để khởi tạo ngẫu nhiên bộ trọng số cho các layer. Khởi tạo trọng số tưởng chừng như là một việc đơn giản nhưng lại hết sức quan trọng. Việc có thể khởi tạo một bộ trọng số "đẹp" và phù hợp có thể giúp mô hình chúng ta hội tụ nhanh hơn rất nhiều. Ngược lại, giá trị khởi tạo tệ sẽ gây khó khăn trong việc tìm kiếm các điểm cực tiểu địa phương hay thậm chí khiến cho mô hình không thể học được.

![image](https://user-images.githubusercontent.com/87894596/230277118-67ef9e3b-6d60-47ce-a617-55096c9dc6dd.png)

Minh họa về Initializers. Việc khởi điểm với một bộ trọng số phù hợp sẽ tạo điều kiện thuận lợi cho mô hình tìm được điểm hội tụ nhanh chóng.

- Trong project này, mình sẽ thực nghiệm kết quả đạt được khi sử dụng các Activation functions/Initializers khác nhau thông qua việc xây dựng và đánh giá một mô hình multilayer perceptrons dùng để phân loại cảm xúc dựa trên ảnh gương mặt của một người nào đó. 
- Input/Output của bài toán như sau:
  - Input: Ảnh gương mặt một người (Ở định dạng ảnh mức xám).
  - Output: Cảm xúc của người đó (chuỗi kí tự).

- Bộ dữ liệu dùng để huấn luyện, đánh giá cho mô hình của chúng ta là bộ dữ liệu FER 2013. Bộ dữ liệu FER 2013 gồm có tổng 35.887 mẫu dữ liệu với 7 classes tượng trưng cho 7 cảm xúc khác nhau (’angry’, ’disgust’, ’fear’, ’happy’, ’neutral’, ’sad’, ’surprise’) và đã được chia sẵn hai bộ dữ liệu train (28704 mẫu dữ liệu) và val (7178 mẫu dữ liệu).

- Kiến trúc mạng sử dụng chung cho thực nghiệm:

![image](https://user-images.githubusercontent.com/87894596/230277846-ac9b1772-98d9-4ee7-913a-99a9464f9398.png)

- Kết quả nghiệm thu được:

  - Giữa các activation khác nhau:

  ![image](https://user-images.githubusercontent.com/87894596/230277986-5d15fde0-83ca-467d-b7c5-dd68f6995094.png)


  - Giữa các initializers khác nhau:

  ![image](https://user-images.githubusercontent.com/87894596/230278079-68d842b8-e567-4d60-b018-c63015d46bfe.png)

  - So sánh giữa khởi tạo zeros, ones, hằng số:
  
  ![image](https://user-images.githubusercontent.com/87894596/230278304-aea63d09-e9c4-43e9-b055-3710c7b86ff9.png)

