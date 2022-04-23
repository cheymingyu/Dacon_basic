# Dacon_basic
데이콘 베이직 연습

***
구글 드라이브에서 코랩으로 데이터 다운받기
```python
# 라이브러리 설치
!pip install gdrive_dataset

from gdrivedataset import loader

file_id = "구글드라이브 파일 id"
loader.load_from_google_drive(file_id)
```

결측치 확인하기
```python
def check_missing_value(df):
  missing_values = df.isnull().sum().sort_values(ascending=False)
  missing_percentage = (missing_values / len(df)) * 100
  result = pd.concat([missing_values, missing_percentage], axis=1, keys=['Missing values', '% Missing'])
  display(result)
check_missing_value(train)
```
