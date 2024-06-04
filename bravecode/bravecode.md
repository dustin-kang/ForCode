# 1. 입출력

### 나누어 입력받기
```py
a, b = map(int, input().split())
```

### 입출력 가속
```py
from sys import stdin, stout

N = int(stdin.readline()) # 정수 입력을 받고
stout.write(str(N)) # 문자열 출력
```

### 배열 입력
```py
MAP = [list(map(int, input().split())) for _ in range(int(input()))]
```
```
3
1 2 3
4 5 6
7 8 9
>>> MAP
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

### 리스트에 문자열 입력
```py
apple = list(input()) #APPLE
# ['A', 'P', 'P', 'L', 'E']
```

### 배열 출력
```py
arr = [1,2,3,4]
print("".join(map(str, arr))) # 1234
```

```py
print(*arr) # 1 2 3 4
```

# 2. 정수와 문자열
### 최대값 최소값 구하기
```py
ans = 2
for num in arr:
    if ans > num:
        ans = num
print(ans) # 최소값
```

### 진법 변환

```py
print(bin(42), oct(42), hex(42))
# 0b101010 0o52 0x2a

int('0b101010', 2) # 60
```

### 문자열 변환

```py
alph = "ABCD"
alph[::-1] # DCBA
```

```py
ord('A') # 65 문자 -> 아스키
chr(90) # 'Z' 아스키 -> 문자
```

# 3. 배열

### 배열 초기화
```py
N, M = map(int, input().split()) # 2 3
arr = [[0] * N for _ in range(M)]

# [[0, 0], [0, 0], [0, 0]]
```

### 배열 뒤집기
- `reverse`는 인덱스를 이용한 방식(`[::-1]`) 보다 빠르다. 
```py
arr = list(map(str, list('APPLE'))) # ['A', 'P', 'P', 'L', 'E']

arr.reverse() # ['E', 'L', 'P', 'P', 'A']

arr = [int(i) for i in '1234'] # [1,2,3,4]
```

### 배열 정렬
```py
arr.sort()
arr.sort(reverse=True)

arr.sort(key=lambda x : (x[0], x[1])) # 0, 1 번째 데이터를 오름차 순

arr.sort(key = lambda x : (x[0], -x[2], x[1])) # 0 2(내림차) 1 순으로 오름차순
```

