---
title: python_bfs 문제 풀 때 tip
tags: boj
comments: true
categories: problem_solving
---

#### 2차원 배열로 입력이 주어지는 경우, 입력 받는 방법.
1) 배열 원소가 떨어져 있을 때 
```python
''' 
sample_input
0 0 0 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
0 0 0 0 0 1
'''
input = sys.stdin.readline()
h, w = map(int, input.split())

arr = []
for i in range(h):
  arr.append(list(map(int, input.split()))) #split 후에 list로 변환
  #for j in range(w):
```  
2) 배열 원소가 붙어서 주어져 있을 때

```python
'''
sample_input
101111
101010
101011
111011
'''
input = sys.stdin.readline()

arr = []
for _ in range(h):
  arr.append(input)
```

#### 큐의 push와 pop
1) 리스트를 큐로 활용하는 경우  
```python
def bfs():
  q = [(0, 0)] # 초기 입력 값 예시
  
  while q:
    y, x = q.pop(0) # 첫번째 원소 pop
    ...
    q.append((ny, nx)) # ny, nx는 예시
```
  
2) `deque`을 이용하는 경우  
```python
from collections import deque

def bfs():
  while q:
    y, x = q.popleft()
    ...
    q.append((ny, nx)) # ny, nx는 예시
```
