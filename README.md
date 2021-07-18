
# Cài đặt
* Cài đặt [Python 2.7] (https://www.python.org/downloads/) trên Linux và Windows.
* Vì chương trình được viết bằng Python 2.7, nên trước tiên phải cài đặt python 2.7 với công cụ pip. Glycation sử dụng các phụ thuộc sau: numpy, pandas, matplotlib, scipy và scikit-learning. Trước tiên, bạn có thể cài đặt các gói này bằng các lệnh sau:
```
pip install numpy
pip install pandas
pip install matplotlib
pip install scipy
pip install scikit-learn
```
* Nếu bạn gặp lỗi sau khi nhập các lệnh trên trong Linux, nội dung cụ thể như sau:
</br> Unable to install packages due to Environment Error: [Errno 13] Permission denied: '/usr/local/lib/python2.7/dist-packages/sklearn'
 sử dụng tùy chọn '--user' hoặc kiểm tra các quyền.
</br> Người dùng có thể thay đổi các lệnh thành:
```
pip install numpy --user
pip install pandas --user
pip install matplotlib --user
pip install scipy --user
pip install scikit-learn --user
```

Chạy PredGly
mở cmd trong Windows hoặc Linux, sau đó chuyển vào thư mục PredGly-master / Code chứa predict.py
</br> ** Đối với dự đoán vị trí glycation gõ lệnh : **
</br> `python predict.py -input [custom predicting data in txt format] -threshold [threshold value] -output [ predicting results in csv format]`
</br> ** Ví dụ: **
</br> `python predict.py -input ../codes/example.txt -threshold 0.5 -output ../codes/results.csv`
</br> -output là tham số tùy chọn, trong khi -input và -threshold là các tham số bắt buộc. Kết quả dự đoán sẽ hiển thị trong cmd hoặc terminal và nếu bạn không muốn lưu kết quả, bạn không cần input -output.

</br>**Ví dụ:**
</br>`python predict.py -input ../codes/example.txt -threshold 0.5`

</br>**Để biết chi tiết về -input, -threshold và -output, hãy chạy::**
</br>`python predict.py -h`

Thông báo
* Để nhận được kết quả dự đoán, vui lòng lưu trình tự protein truy vấn và tên protein ở định dạng txt. Người dùng có thể tham khảo example.txt trong thư mục mã. Cũng cần lưu ý, mỗi tên protein nên được thêm vào bởi '>', nếu không chương trình sẽ xảy ra lỗi.
* Các axit amin được chấp nhận là: A, C, D, E, F, G, H, I, K, L, M, N, P, Q, R, S, T, V, W, Y và ảo axit amin O. Nếu đoạn prôtêin chứa các axit amin khác, chương trình chỉ dự đoán các đoạn có chứa 21 axit amin nói trên.
* Để lưu kết quả dự đoán,-đầu ra phải ở định dạng csv.
