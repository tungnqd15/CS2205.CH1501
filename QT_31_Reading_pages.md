# QT31: READING PAPERS #1

## HSA-RNN: Hierarchical Structure-Adaptive RNN for Video Summarization 
Bin Zhao, Xuelong Li, Xiaoqiang Lu

https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Zhao_HSA-RNN_Hierarchical_Structure-Adaptive_CVPR_2018_paper.pdf

![CVPR_core_ranking](https://user-images.githubusercontent.com/79246748/118426941-5e958780-b6f6-11eb-9ff6-a2210d9e749f.png)


## 1. Bài toán mà bài báo giải quyết là gì? 

- Dữ liệu video tăng, cần phát triển công cụ tóm tắt video (video summarization)
- Tóm tắt video nhằm mục đích kiểm duyệt và hiểu một video dài bằng cách rút ngắn nó thành một phiên bản nhỏ gọn, tức là, làm nổi bật bản chất và loại bỏ sự dư thừa. 
- Có 3 hướng tiếp cận, đó là cảnh quay (shots), khung hình (frames) và các đối tượng (objects). 
- Bài báo tập trung vào một số cảnh quay chính (several key shots), vì có thể bảo tồn thông tin và tính nhất quán theo không gian-thời gian của nội dung video. 
- Đề xuất phương pháp khai thác cấu trúc video và tóm tắt nội dung video
- Dùng LSTM trượt hai chiều (bidirectional LSTM) để phát hiện các ranh giới trong video, phân đoạn chính xác của các video dài với LSTM, do đó vấn đề độ dốc kích thích được giảm thiểu.
- Tập dữ liệu sử dụng: SumMe TVum, CoSum và VTW. 
- 
## 2. Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?

- phân nhóm các shot tương đồng


## 3. Ý tưởng giải quyết là gì?

Cách tiếp cận: hai lớp (layers)
- khai thác cấu trúc video (exploit the video structure)
  - cấu trung phân cấp (hierarchical): (frames form shots and shots form video)
  - sự phụ thuộc về thời gian giữa các khung hình.
  - Không khả thi khi áp dụng bidirectional LSTM (đánh mất thông tin quan trọng)
  ![Bi_LSTM](https://user-images.githubusercontent.com/79246748/118460404-de3b4a80-b726-11eb-836b-53f1eef8b2e3.png)

- tóm tắt video (summarize the video)

sliding bidirectional LSTM
 

## Reference 

https://cseweb.ucsd.edu/~wgg/CSE210/howtoread.html

https://www.huffpost.com/entry/how-to-read-and-understand-a-scientific-paper_b_5501628

