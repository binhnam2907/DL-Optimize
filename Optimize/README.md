GG Drive link cho colab: https://drive.google.com/drive/folders/105QyK9zUY8TBHmxDFqFcmo2KHkSAMGGt?usp=sharing

### Trong project này, mình xây dựng một số hàm optimize cơ bản được sử dụng nhiều trong Deeplearning

1. Gradient Descent: Là thuật toán đi tìm điểm minimum của một function dụa trên tính toán gradient của function đó. Function này phải thỏa mãn điều kiện là liên tục và có thể đạo hàm được phần lớn ở mọi nơi. Phương pháp này ta sẽ chọn một điểm xuất phát ngẫu nhiên (1 điểm bất kỳ trên function) sau đó dựa vào độ dốc và hướng của gradient để đi ngược hướng và tiến về nơi có vị trị thấp hơn, việc này được lặp đi lặp lại cho đến khi tìm được điểm minimum hoặc thỏa mãn điều kiện dừng.

![image](https://user-images.githubusercontent.com/87894596/230279039-7dcb97b8-bec9-4cbb-82db-ff91092a73d8.png)

2. Gradient Descent + Momentum: Phương pháp này khắc phục điểm yếu của Gradient Descent là không thể vượt qua local minimum để tiến về điểm local minimum khác thấp hơn. Gradient Descent + Momentum sử dụng exponentially weighted average gradient để tích lũy gradient từ trước đó và kết hợp với gradient hiện tại giúp tạo ra một giá trị đủ lớn vượt qua local minimum hiện tại và tiến về local minimum tốt hơn. Nó hoạt động tương tự như viên bi có khi lăn xuống kết hợp thêm đà (momentum) để vượt qua dốc và rơi vào nơi tốt hơn.

![image](https://user-images.githubusercontent.com/87894596/230279110-9af0d7c8-9ca6-44a5-902d-92de5e1cc74f.png)

3. RMSProp:

![image](https://user-images.githubusercontent.com/87894596/230279157-bfb477b2-f3f3-44b2-8601-403532fa19d2.png)

  Đây là thuật toán mở rộng từ AdaGrad và cũng sử dụng gradient từ trước để tạo ra một thuật toán có thể adaptive learning rate thay vì learning rate cố định như các thuật toán trước. Ý tưởng chính của RMSProp là sử dụng exponentially weighted average bình phương gradient và chia gradient với căn bậc hai của average này.

4. Adam: Có thể xem Adam là thuật toán sử dụng kết hợp ý tưởng của Momentum và RMSProp vì Adam sử dụng exponentially weighted average gradient và exponentially weighted average bình phương gradient. Cách thức Adam hoạt động theo việc thừa hưởng điểm mạnh của momentum và adaptive learning rate, momentum giúp vượt qua các local minimum để tiến đến các local minimum tốt hơn, trong khi adaptive learning rate giúp cho việc hội tụ nhanh hơn thay vì phải mất một khoảng thời gian để dao động xung quanh điểm hội tụ.

![image](https://user-images.githubusercontent.com/87894596/230279331-c2c6f099-4112-472e-85a7-adb98d53b950.png)
