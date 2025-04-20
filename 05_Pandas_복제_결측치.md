# 1. copy
- df2 = df 의 경우 (shallow copy)
- df2 = df.copy() 를 해야 deep copy

# 2. 결측치 확인
- 결측치 : 비어있는 데이터

## isnull(), isna()
- df.isnull()
	- True = 1
	- False = 0
	- df.isnull().sum() 하면 결측치 수가 나옴
- isna() : isnull()과 완전 동일한 동작을 함

## notnull()
- isnull() 반대

## fillna()
- 결측치에 대하여 일괄적으로 값을 채울 수 있음
- df1['age'] = df1['age'].fillna(700)
	- age column의 결측치가 일괄적으로 700으로 채워짐
	- 추천되는 방식
- df1['age'].fillna(700, inplace=True)
	- 값이 대체됨
- 대입하거나 값을 대체하는 방식으로 적용 가능
- df1['age'].fillna(df1['age'].mean()).tail()
- df1['age'].fillna(df1['age'].median()).tail()
- 최빈값(mode)
	- 반드시 0번째 index 지정해서 채워야 함
	- df1['deck'].fillna(df1['deck'].mode()[0])

## dropna()
- 1개라도 NaN값이 있는 행을 제거
- df1.dropna()
- 기본은 how=any
	- any : 1개라도 NaN값이 존재시 drop
	- all : 모두 NaN값이 존재시 drop