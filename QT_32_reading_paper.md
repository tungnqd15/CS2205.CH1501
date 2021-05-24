# QT32: READING PAPER #2

## Joint Learning of Named Entity Recognition and Entity Linking
by Pedro Henrique Martins - Zita Marinho - André F.T. Martins 

https://www.aclweb.org/anthology/P19-2026.pdf

![core_eacl](https://user-images.githubusercontent.com/79246748/119259556-016b6b80-bbf9-11eb-8835-473c42f9cc39.png)

## 1. Bài toán là gì?

### Named Entity Recognition (NER)

> Named Entity Recognition, là tác vụ cơ bản trong lĩnh vực Xử lý ngôn ngữ tự nhiên. Vai trò chính của tác vụ này là nhận dạng các cụm từ trong văn bản và phân loại chúng vào trong các nhóm đã được định trước như tên người, tổ chức, địa điểm, thời gian, loại sản phẩm, nhãn hiệu, vân vân và vân vân... Từ kết quả của task vụ NER có thể xử lý cho nhiều bài toán phức tạp hơn như Chatbot, Question Answering, Search,...

![named_entity_recognition](https://user-images.githubusercontent.com/79246748/119311276-0f71c880-bc9b-11eb-9818-fbf57094f3b5.png)

### Entity Linking (EL)

![entity_linking](https://user-images.githubusercontent.com/79246748/119311842-c2dabd00-bc9b-11eb-948f-9b1b376bb10a.png)

> Leveraging the relationship between Named-Entity Reconigtion (NER) and Entity Linking (EL) to improves the performance in both tasks.

## 2. Problem là gì? 

> In order to perform EL, first the mentions to entities had to be detected. However, most entity linking approaches disregard the mention detection part, assuming that the correct mentions have been previously detected.

## 3. Ý tưởng của kỹ thuật giải quyết là gì?

> Base model: Stack-LSTM

> Modification:
  - NER: Words in Stack -> hidden state (bi-LSTM 1) -> Attention score
  - [Stack-LSTM; Attention score] --Affine--> Prediction (Action)

> EL: Action predicted in NER step is Reduce (detected a mention of NER, need to be disambiguated)

## reference
