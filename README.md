# Dacon_basic
데이콘 베이직 연습

***
구글 드라이브에서 코랩으로 데이터 다운받기
```python
# 라이브러리 설치
!pip install gdrive_dataset

from gdrivedataset import loader

file_id = "1RDAVsCCQCs1bxjq_2Q6qPlGeztnQ2AMD"
loader.load_from_google_drive(file_id)
```
