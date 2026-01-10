## 배열(Array)
동일한 데이터 타입의 요소들을 연속된 메모리 공간에 순서대로 저장하는 자료구조이다.
+ 데이터 조회에서 O(1)의 시간 복잡도를 가진다.

## 장점
+ 연속된 메모리 공간을 사용하므로 첫 데이터의 주소만 알면 나머지 요소에도 빠르게 접근 가능
+ 인덱스를 통한 빠른 접근 속도
## 단점
+ **크기가 고정**되어 있어 동적 크기 변경이 어렵다
+ 중간에 데이터를 추가/삭제할 경우 요소 이동이 필요해 비효율적
## 연결리스트 (Linked List)
각각의 데이터가 메모리 공간 상에 **고유한 노드**로 존재하며,
각 노드는 **다음(또는 이전) 노드의 메모리 주소**를 저장하고 있는 구조이다.\
즉, **노드들이 서로 연결되어 있는 구조**
+ 데이터 조회 시 순차적으로 탐색하기 때문에 O(N)의 시간 복잡도
+ 데이터 추가와 삭제에는 O(1)의 시간 복잡도

## 장점
+ 크기가 동적으로 변경 가능하다.
+ 중간에 데이터 추가·삭제가 빠르고 효율적이다.
+ 메모리를 필요한 만큼만 사용 가능하다.

## 단점
+ 순차 탐색 구조로 인해 조회 속도가 느리다.
+ 포인터(주소)를 저장해야 하므로 추가적인 메모리 공간 필요하다.
+ 구조가 배열보다 복잡하여 구현 난이도가 높다.

![alt text](<../image/array, linkedlist.png>)

## 코드
```python
# Array (배열) 예제

print("=== Array ===")
arr = [10, 20, 30]

# 조회 O(1)
print("조회:", arr[1])

# 추가
arr.append(40)
print("추가:", arr)

# 삽입 (중간) O(N)
arr.insert(1, 15)
print("삽입:", arr)

# 삭제 O(N)
arr.remove(30)
print("삭제:", arr)
```

```python
# Linked List (연결 리스트)

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


class LinkedList:
    def __init__(self):
        self.head = None

    # 추가
    def append(self, data):
        new_node = Node(data)

        if not self.head:
            self.head = new_node
            return

        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = new_node

    # 조회
    def search(self, target):
        cur = self.head
        idx = 0

        while cur:
            if cur.data == target:
                return idx
            cur = cur.next
            idx += 1

        return -1

    # 삭제
    def delete(self, target):
        cur = self.head

        if cur and cur.data == target:
            self.head = cur.next
            return

        prev = None
        while cur:
            if cur.data == target:
                prev.next = cur.next
                return
            prev = cur
            cur = cur.next

    # 출력
    def print_list(self):
        cur = self.head
        while cur:
            print(cur.data, end=" -> ")
            cur = cur.next
        print("None")
```