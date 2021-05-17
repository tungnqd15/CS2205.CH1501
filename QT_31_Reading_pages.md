# QT31: READING PAPERS #1

## HSA-RNN: Hierarchical Structure-Adaptive RNN for Video Summarization 
Bin Zhao, Xuelong Li, Xiaoqiang Lu

https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Zhao_HSA-RNN_Hierarchical_Structure-Adaptive_CVPR_2018_paper.pdf

![CVPR_core_ranking](https://user-images.githubusercontent.com/79246748/118426941-5e958780-b6f6-11eb-9ff6-a2210d9e749f.png)


## 1. Bài toán mà bài báo giải quyết là gì? 
- Dữ liệu video tăng, cần phát triển công cụ tóm tắt video (video summarization)
- Tóm tắt video nhằm mục đích kiểm duyệt và hiểu một video dài bằng cách rút ngắn nó thành một phiên bản nhỏ gọn, tức là, làm nổi bật bản chất và loại bỏ những đoạn dư thừa. 
- Cấu trúc video: cảnh quay (shots), khung hình (frames) và các đối tượng (objects). Kỹ thuật hiện tại không khai thác cấu trúc này 
- Bài báo này tập trung vào một số cảnh quay chính (several key shots), vì phản ánh thông tin nhất quán với nội dung video. 
- Dùng LSTM trượt hai chiều (bidirectional LSTM) để phát hiện các ranh giới (detected shot boundaries) trong video, phân đoạn chính xác hơn so với LSTM.
- Tập dữ liệu sử dụng: SumMe TVum, CoSum và VTW.  
## 2. Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?

- phân nhóm các shot tương đồng

## 3. Ý tưởng giải quyết là gì?

![HSA-RNN](https://user-images.githubusercontent.com/79246748/118468649-2eb6a600-b72f-11eb-9d7d-6b93c933a937.png)

### Video Structure Exploitation
Khai thác cấu trúc video (exploit the video structure) - phân cấp (hierarchical): 
- Các đối tượng trong khung hình 
- Các khung hình cấu thành cảnh quay (frames form shots)
- Các cảnh quay cấu thành video (shots form video)

A sliding bidirectional LSTM

1) Thao tác trượt cho phép LSTM ngắn xử lý video dài. Nó tránh khai thác phụ thuộc theo thời gian giữa hàng nghìn khung hình, điều này có thể giảm thiểu vanishing gradient problem.

2) LSTM hai chiều cùng ghi lại thông tin về phía trước và phía sau trong trình tự khung hình, có thể bảo vệ ranh giới cảnh quay một cách hiệu quả.

3) LSTM trượt hai chiều chỉ xử lý các khung cục bộ ở mỗi bước, điều này làm giảm sự can thiệp của thông tin toàn cầu không liên quan. Cụ thể, ở bước đầu tiên, LSTM hai chiều hoạt động trên thứ tự khung (f 1, f 2,.., F k) theo các phương trình sau, trong đó LSTM (·) là viết tắt của các hoạt động trong mỗi LSTM
đơn vị.

  - sự phụ thuộc về thời gian giữa các khung hình.
  - Không khả thi khi áp dụng bidirectional LSTM (đánh mất thông tin quan trọng)
  ![Bi_LSTM](https://user-images.githubusercontent.com/79246748/118460404-de3b4a80-b726-11eb-836b-53f1eef8b2e3.png)

### Structure-Adaptive Video Summarization

- tóm tắt video (summarize the video)

sliding bidirectional LSTM
 

## Reference 

[1] https://cseweb.ucsd.edu/~wgg/CSE210/howtoread.html

[2] https://www.huffpost.com/entry/how-to-read-and-understand-a-scientific-paper_b_5501628

[3] https://labs.septeni-technology.jp/technote/ml-16-rectifier-linear-function-and-vanishing-gradient-problem/



