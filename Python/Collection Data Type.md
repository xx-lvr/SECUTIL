## 컬렉션 데이터 타입(Collection Data Type)
컬렉션 데이터 타입은 여러 값을 담는 데이터 타입을 말한다.
+ 대표적으로 ```List, Tuple, Set, Dictionary``` 등이 있다.
그리고 이 컬렉션들은 데이터의 수정 가능 여부에 따라 ```Mutable Object```와 ```Immutable Object```로 구분한다.

## Mutable Object
**Mutable Object**는 객체 생성 후 객체를 수정할 수 있다. 대표적인 **Mutable Object**로는 ```List, Dictionary, Set```이다.
```python
my_list = [1, 2, 3, 4, 5] # 리스트 객체 생성, [1, 2, 3, 4, 5]
my_list[4] = 6 # my_list[4]가 6으로 변경
print(my_list) # [1, 2, 3, 4, 6]
```
![alt text](<../image/Mutable Object.png>)

## Immutable Object
**Immutable Object**는 객체 생성 후 객체를 수정할 수 없다. 대표적인 **Immutalbe Object**로는 ```정수, 부동소수점, 문자열, 튜플```이다.
+ 정수는 컬렉션 타입은 아니다.
```python
a = 4   # a = 4
b = a   # a = 4, b = 4 / b는 a가 아닌 a가 참조한 4를 참조
b += 2  # b = 6 / 기존에 참조한 객체를 수정하지 않고 새 객체 6을 참조
print(a, b)  # 4 6
```

## 리스트(List)
**리스트** **Mutable Object**이다. 리스트는 **인덱싱, 슬라이싱**을 할 수 있다.
```python
# 리스트 선언
my_list = [1, 2, 3, 4, 5]
my_list2 = [1, 3, 5] + [7, 9]
my_list3 = list(my_list)
print(my_list)      # [1, 2, 3, 4, 5]
print(my_list2)     # [1, 3, 5, 7, 9]
print(my_list3)     # [1, 2, 3, 4, 5]
```

## 리스트 인덱싱
인덱싱은 인덱스를 활용해서 특정 위치의 원소에 접근하는 것을 말한다.
```python
my_list = [1, 2, 4]
# 값 추가
my_list.append(6) # 6 추가
print(my_list)    # [1, 2, 4, 6]
del my_list[2]    # my_list[2] 삭제
print(my_list)    # [1, 2, 6]
```
## 리스트 슬라이싱
슬라이싱은 시퀀스 자료형의 범위를 지정해서 값들을 복사하여 가져오는 방식을 말한다.\
슬라이싱은 파이썬 코드로 ```list_name[a:b]```와 같이 작성을 한다.
```python
my_list = [1, 2, 3, 4, 5]

# 기본 슬라이싱
print(my_list[0:2])     # [1, 2]
print(my_list[1:])      # [2, 3, 4, 5]
print(my_list[3:4])     # [4]
print(my_list[-4:-2])   # [2, 3]

print(my_list[::1])     # [1, 2, 3, 4, 5] (원본 그대로)
print(my_list[::2])     # [1, 3, 5] (2칸씩 건너뛰기)
print(my_list[1::2])    # [2, 4] (인덱스 1부터 2칸씩)
print(my_list[::-1])    # [5, 4, 3, 2, 1] (역순)
print(my_list[::-2])    # [5, 3, 1] (역순으로 2칸씩)

print(my_list[1:4:2])   # [2, 4] (인덱스 1~3까지, 2칸씩)
print(my_list[0:5:3])   # [1, 4] (인덱스 0~4까지, 3칸씩)
print(my_list[2::-1])   # [3, 2, 1] (인덱스 2부터 역순으로)
print(my_list[4:1:-1])  # [5, 4, 3, 2] (인덱스 4부터 2까지 역순)
```

## 딕셔너리(Dictionary)
**딕셔너리**는 **Mutable Object**로 ```key와 value``` 쌍을 저장하는 해시 테이블로 구현되어 있다.
+ 이름 그대로 **키를 사용하여 값을 검색하는 자료형**이라고 생각하면 된다.

## 딕셔너리 초기화
```python
my_dict = { }
```
## 딕셔너리 삽입과 출력
선언한 딕셔너리에 값을 삽입하고 딕셔너리 전체를 출력한다.
```python
# 딕셔너리 값 삽입
my_dict["apple"] = 1
my_dict["banana"] = 2
my_dict["orange"] = 3
# 딕셔너리 값 출력
print(my_dict)  # {'apple': 1, 'banana': 2, 'orange': 3}
```

## 딕셔너리 검색
```python
key = "apple"
if key in my_dict:
  value = my_dict[key]
  print(f"{key}: {value}")  # apple: 1
else:
  print(f"{key}는 딕셔너리에 존재하지 않습니다.")
```
+ my_dict가 참조하는 딕셔너리의 키들을 보며 ```“apple” 문자열```이 일치하는지 확인하고, 일치하는 키를 찾으면 키-값을 출력한다

## 딕서녀리 수정
```python
my_dict["banana"] = 4
print(my_dict)  # {'apple': 1, 'banana': 4, 'orange': 3}
```
+ ```키 “banana”를 검색```하여 해당 키의 값을 4로 바꾼다. 딕셔너리 내부는 해시 테이블로 구성되어 있으므로 해시 테이블에서 키를 찾거나 하지 않아도 된다.
## 딕서녀리 삭제
```python
del my_dict["orange"]
print(my_dict)  # {'apple': 1, 'banana': 4}
```
+ ```키 “orange”```를 찾아 딕셔너리에서 삭제한다. 딕셔너리에 키가 없는 경우를 처리하는 예외 처리이다. 키가 없는 경우 예외가 발생하므로 예외 처리를 해주어야 한다.


```python
# 딕셔너리 생성
my_dict = {"apple": 1, "banana": 2, "cherry": 3}

# my_dict에 없는 key로 설정
key = "kiwi"

# 키가 딕셔너리에 있는지 확인
if key in my_dict:
    # 키가 딕셔너리에 있으면 해당 값 출력
    print(f"값: {my_dict[key]}")
else:
    # 키가 딕셔너리에 없으면 에러 메시지 출력
    print(f"'{key}' 키가 딕셔너리에 없습니다.")
```

## 튜플(Tuple)
**튜플**은 ```Immutable Object```이다. ```리스트, 딕셔너리```와 달리 한 번 생성하면 삽입하거나 삭제할 수 없다.

## 튜플의 초기화
튜플은 ```( )```를 사용하여 초기화합니다.
```python
my_tuple = (1, 2, 3)
```

## 튜플의 인덱싱, 슬라이싱
튜플은 삽입, 삭제는 되지 않지만 인덱싱, 슬라이싱은 할 수 있습니다. 문법 자체는 리스트와 같다.
```python
my_tuple = (1, 2, 3)

print(my_tuple[0])   # 1
print(my_tuple[1])   # 2
print(my_tuple[2])   # 3

print(my_tuple[1:])    # (2, 3)
print(my_tuple[:2])    # (1, 2)
print(my_tuple[1:2])   # (2,)

print(my_tuple[::-1])  # (3, 2, 1)  역순
print(my_tuple[::2])   # (1, 3)     2칸씩 건너뛰기
print(my_tuple[1::2])  # (2,)       인덱스 1부터 2칸씩
print(my_tuple[-2:])   # (2, 3)     뒤에서 2개
print(my_tuple[-3:-1]) # (1, 2)     인덱스 -3부터 -2까지
print(my_tuple[0:3:2]) # (1, 3)     인덱스 0~2까지, 2칸씩
```