## 빌트인 데이터 타입(Built-In Data Type)
언어 자체에서 제공하는 데이터 타입과 컬렉션 데이터 타입이 있다.
+ 기본 데이터 타입으로는 ```정수형(int), 부동소수형(float), 문자열 타입```이 있다.
+ 컬렉션 데이터 타입으로는 ```리스트, 튜플, 셋, 딕셔너리``` 등이 있다.

## 정수형
정수형은 양과 음의 정수, 0을 포함한다.
+ 정수형은 더하기, 빼기, 곱하기, 나누기와 같은 사칙 연산 외 많은 연산을 할 수 있다.
```python
# 선언
a = 13
b = 4
# 연산
print(a + b)  # 더하기 / 17
print(a - b)  # 빼기 / 9
print(a * b)  # 곱하기 / 52
print(a / b)  # 나누기 (소수점 포함) / 3.25
print(a // b)   # 나누기 (소수점 제외) / 3
print(a % b)    # 모듈러 연산 (나머지) / 1
print(-a)   # 부호를 바꿈 / -13
print(abs(-a))  # 절대값 / 13
print(a**b) # a의 b승 / 28561
# 비교 연산
print(a == b)   # 같은 값인지 비교 / False
print(a != b)   # 같지 않은 값인지 비교 / True
print(a > b)    # 왼쪽 값이 더 큰지 비교 / True
print(a < b)    # 왼쪽 값이 더 작은지 비교 / False
print(a >= b)   # 왼쪽 값이 더 크거나 같은지 비교 / True
print(a <= b)   # 왼쪽 값이 더 작거나 같은지 비교 / False
# 정수형 비트 연산
print(a & b)    # AND / 4
print(a | b)    # OR / 13
print(a ^ b)    # XOR / 9
print(~a)   # NOT / -14
print(a << 2)   # 왼쪽 시프트 (a에 2^2를 곱한 것과 동일)  / 52
print(a >> 1)   # 오른쪽 시프트 (a를 2^1로 나눈 것과 동일) / 6
# 정수형 논리 연산
print(a and b)  # 논리 연산 AND / 4
print(a or b)   # 논리 연산 OR / 13
print(not a)    # 논리 연산 NOT / False
```
## 부동소수형
부동소수형은 소수를 저장할 때 사용한다.
```python
# 사칙연산
print(2.5 + 3.7)    # 더하기 / 6.2
print(7.9 - 4.2)    # 빼기 / 3.7
print(1.5 * 4.8)    # 곱하기 / 7.199999999999999
print(10.0 / 3.2)   # 나누기 / 3.125
# 정수형 나누기, 모듈러, 제곱 연산
print(10.0 // 3.2)  # 정수형 나누기 / 3.0
print(10.0 % 3.2)   # 모듈러  / 0.39999999999999947
print(2.0 ** 3.2)   # 제곱 연산 / 9.18958683997628
# 논리 연산
x = 0.5
y = 1.2
z = 2.0
print(x > y and y < z)  # AND 연산 / False
print(x < y or y < z)   # OR 연산 / True
print(not (x > y))  # NOT 연산 / True
```