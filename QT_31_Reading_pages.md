# QT31: READING PAPERS #1

## HSA-RNN: Hierarchical Structure-Adaptive RNN for Video Summarization 
Bin Zhao, Xuelong Li, Xiaoqiang Lu

https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Zhao_HSA-RNN_Hierarchical_Structure-Adaptive_CVPR_2018_paper.pdf

![CVPR_core_ranking](https://user-images.githubusercontent.com/79246748/118426941-5e958780-b6f6-11eb-9ff6-a2210d9e749f.png)


## 1. Bài toán mà bài báo giải quyết là gì? 

> Dữ liệu video tăng, cần phát triển công cụ tóm tắt video (video summarization) nhằm mục đích kiểm duyệt và hiểu một video dài bằng cách rút ngắn nó thành một phiên bản nhỏ gọn.

- Input: một video (frame feature sequence $(f_1,f_2,\dots,f_n)$)
- Output: những cảnh quay trong video (shot feature sequence $(s_1,s_2,\dots,s_m)$) 

trong đó n và m là số khung hình (frames) và cảnh quay (shots)

> Cấu trúc video: cảnh quay (shots), khung hình (frames) và các đối tượng (objects). Kỹ thuật hiện tại không khai thác cấu trúc này.

> Bài báo này tập trung vào một số cảnh quay chính (several key shots), vì phản ánh thông tin nhất quán với nội dung video. 

> Tập dữ liệu sử dụng: SumMe TVum, CoSum và VTW.  

## 2. Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?

> Cấu trúc dữ liệu của một video như thế nào? 

- Khai thác cấu trúc frames và shots

> Làm thế nào để xác định các phân cảnh (shots) thể hiện đúng nội dung video đầu vào?

- Sử dụng HSA-RNN với 2 layers (sliding bidirectional LSTM và bidirectional LSTM)


## 3. Ý tưởng giải quyết là gì?

Khai thác cấu trúc video (exploit the video structure) - phân cấp (hierarchical): 
- Các đối tượng trong khung hình (objects form frames)
- Các khung hình cấu thành cảnh quay (frames form shots)
- Các cảnh quay cấu thành video (shots form video)

### Hierarchical Structure-Adaptive RNN

![HSA-RNN](https://user-images.githubusercontent.com/79246748/118468649-2eb6a600-b72f-11eb-9d7d-6b93c933a937.png)

#### Layer 1. Sliding bidirectional LSTM

> Layer thứ nhất sử dụng sliding bidirectional LSTM nhằm xác định ranh giới các cảnh quay (detected shot boundaries), cắt video thành các phân cảnh (shot feature).

> Sliding bidirectional LSTM xử lý video dài tốt hơn long single LTSM, tránh vanishing gradient problem.

![long_single_LSTM_vs_sliding_bi_LSTM](https://user-images.githubusercontent.com/79246748/118475498-873d7180-b736-11eb-9e06-7520c493c802.png)

> Sliding bidirectional LSTM chỉ xử lý các khung cục bộ (local frames) trên mỗi bước, giảm ảnh hưởng của global information không liên quan.

#### Layer 2. Bidirectional LSTM

![Bi_LSTM](https://user-images.githubusercontent.com/79246748/118460404-de3b4a80-b726-11eb-836b-53f1eef8b2e3.png)

> Layer thứ 2 sử dụng bidirectional LSTM , dùng để tóm tắt video (video summarization) dự đoán shots đại diện nội dung video.


## Reference 

[1] https://cseweb.ucsd.edu/~wgg/CSE210/howtoread.html

[2] https://www.huffpost.com/entry/how-to-read-and-understand-a-scientific-paper_b_5501628

[3] https://labs.septeni-technology.jp/technote/ml-16-rectifier-linear-function-and-vanishing-gradient-problem/


