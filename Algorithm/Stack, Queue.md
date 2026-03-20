## 스택(Stack)
**스택**은 **후입선출(LIFO, Last In First Out)방식**으로 작동하는 선형 자료구조이다.
+ ```top(peek)```: 가장 최근에 저장된 데이터이자 먼저 삭제 될 데이터이다.
+ ```push```: 데이터를 삽입하는것을 말하며 삽입 된 데이터는 삭제시 가장 먼저 삭제 될 데이터가 된다.
+ ```pop```: 데이터를 삭제할 때 사용하며 가장 최근에 저장된 데이터가 삭제된다.
## 사용 예
+ 브라우저의 뒤로가기
+ 실행 취소 (Ctrl + z)
+ 재귀 함수
+ 역순 문자열 (문자열 거꾸로 뒤집기)

![alt text](<../image/stack, queue.png>)
## 큐(Queue)
**큐**는 **선입선출(FIFO, First In First Out)방식**으로 작동하는 선형 자료구조이다.
+ ```Enqueue```: 데이터 삽입
+ ```Dequeue```: 데이터 삭제
+ ```Front```: Dequeue시 삭제되는 데이터 (가장 먼저 저장된 데이터)를 가르킵니다.
+ ```Rear```: 추가될 새로운 요소의 위치를 가르킵니다.
## 사용 예
+ BFS 알고리즘
+ 프로세스 관리
+ 프린터의 대기열

## 구현
```python
# Stack
class Stack:
    def __init__(self):
        self.stack = []

    def push(self, value):
        self.stack.append(value)  # 삽입

    def pop(self):
        if self.is_empty():
            return "Stack is empty"
        return self.stack.pop()   # 삭제

    def peek(self):
        if self.is_empty():
            return "Stack is empty"
        return self.stack[-1]     # top 확인

    def is_empty(self):
        return len(self.stack) == 0

    def size(self):
        return len(self.stack)
```
```python
# Queue
class Queue:
    def __init__(self):
        self.queue = []

    def enqueue(self, value):
        self.queue.append(value)   # 삽입

    def dequeue(self):
        if self.is_empty():
            return "Queue is empty"
        return self.queue.pop(0)   # 삭제

    def front(self):
        if self.is_empty():
            return "Queue is empty"
        return self.queue[0]

    def is_empty(self):
        return len(self.queue) == 0

    def size(self):
        return len(self.queue)
```