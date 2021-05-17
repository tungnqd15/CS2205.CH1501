# QT31: READING PAPERS #1

## HSA-RNN: Hierarchical Structure-Adaptive RNN for Video Summarization 
Bin Zhao, Xuelong Li, Xiaoqiang Lu

https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Zhao_HSA-RNN_Hierarchical_Structure-Adaptive_CVPR_2018_paper.pdf

![CVPR_core_ranking](https://user-images.githubusercontent.com/79246748/118426941-5e958780-b6f6-11eb-9ff6-a2210d9e749f.png)


## 1. Bài toán mà bài báo giải quyết là gì? 

- dữ liệu video đang tăng 
- video tóm tắt là một trong những
các công cụ vượt qua thách thức này.

Tóm tắt video cung cấp cho chúng tôi một cách hiệu quả để
duyệt và hiểu một video dài bằng cách rút ngắn nó thành
một phiên bản nhỏ gọn, tức là, làm nổi bật bản chất và loại bỏ sự dư thừa. 

Thực tế, video tóm tắt có thể cô đọng video ở ba cấp độ, đó là cảnh quay, khung hình
và các đối tượng. 

Trong bài báo này, chúng tôi tập trung vào phần đầu tiên tóm tắt video với một số cảnh quay chính (several key shots), vì nó có thể bảo tồn tốt hơn thông tin động và tính nhất quán theo không gian-thời gian của nội dung video. 

1) Theo hiểu biết của chúng tôi, chúng tôi là người đầu tiên đề xuất phương pháp tóm tắt video thích ứng theo cấu trúc mà chung-ly khai thác cấu trúc video và tóm tắt nội dung video. Nó có thể tạo nên điểm yếu của các phương pháp tiếp cận hiện có trong việc khai thác cấu trúc video và cải thiện hơn nữa chất lượng cơ bản.

2) Chúng tôi thiết kế một LSTM trượt hai chiều để phát hiện các ranh giới trong video. Nó đạt được phân đoạn chính xác của các video dài với LSTM ngắn hơn nhiều, do đó vấn đề độ dốc kích thích được giảm thiểu.

3) Tập dữ liệu: SumMe TVum, CoSum và VTW
4) 
Minh hoạ input/output


## 2. Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?

- phân nhóm các shot tương đồng

## 3. Ý tưởng giải quyết là gì?

Minh hoạ trực quan

## Reference 

https://cseweb.ucsd.edu/~wgg/CSE210/howtoread.html

https://www.huffpost.com/entry/how-to-read-and-understand-a-scientific-paper_b_5501628

