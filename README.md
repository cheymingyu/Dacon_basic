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

데이터프레임 행/열 전부 표시하기
```python
pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)

# 직접 지정
pd.options.display.columnss = 10
pd.options.display.max_rows = 10
```
