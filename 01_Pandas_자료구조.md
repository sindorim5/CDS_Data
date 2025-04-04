# 1. Pandas란?

## 엑셀보다 Pandas를 사용하는 이점

- 대용량 데이터 처리시 엑셀보다 처리 속도가 빠름
- 자동화
  - 수 많은 복잡한 데이터 처리 과정을 자동화 할 수 있음
- 엑셀에서 지원하지 않는 복잡한 테스크 수행 가능
  - 파이썬 외장 라이브러리를 활용한 고급 전처리 적용
- 다양한 라이브러리와의 호환성
  - 웹크롤러, 넘파이(Numpy), 머신러닝(scikit-learn), 딥러닝(tensorflow, pytorch) 등

# 2. 자료구조

## Series
- 1차원 자료구조
- index와 같이 표기하며 dtype(데이터 타입)을 가짐

## DataFrame
- 2차원 자료구조
- index, column과 같이 표기됨
- 각 column별 각각의 dtype(데이터 타입)을 가짐
- Series가 2개 이상 묶이면 DataFrame
