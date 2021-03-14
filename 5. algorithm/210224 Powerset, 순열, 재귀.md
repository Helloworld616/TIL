## 1. Powerset 재귀

```python
N = 3

arr = [1, 2, 3] # 우리가 활용할 데이터

sel = [0] * N # 내가 해당 원소를 뽑았는지 체크하는 리스트

def powerset(idx):
    if idx == N:
        print(sel, ":", end = " ")
        for i in range(N):
            if sel[i]:
                print(arr[i], end = ' ')
        print()
        
        return 
    
    # idx 자리의 원소를 뽑고 간다.
    sel[idx] = 1
    powerset(idx + 1)
    sel[idx] = 0
    powerset(idx + 1)
    
powerset(0)
```



## 2. 백트래킹을 이용한 순열 구하기

```python
arr = [1, 2, 3]

N = 3

sel = [0] * N # 결과들이 저장될 리스트
check = [0] * N # 해당 원소를 이미 사용했는지 안했는지에 대한 체크

def perm(idx):
    # 다 뽑아서 정리했다면
    if idx == N:
        print(sel)
    else:
        for i in range(N):
            if check[i] == 0:
                sel[idx] = arr[i] # 값을 써라
                check[i] = 1 # 사용을 했다는 표시
                perm(idx+1)
                check[i] = 0 # 다음 반복문을 위한 원상복구
       
```



## 3. 비트를 이용한 순열 구하기

```python
arr = [1, 2, 3]

N = 3

sel = [0] * N

# check: 10진수 정수
def perm(idx, check):
    if idx == N:
        print(sel)
        return 
    
   	for i in range(N):
        # j번째 원소를 활용했군. 그럼 쓰면 안 되지.
        if check & (i<<j): 
            continue
        
        sel[idx] = arr[j]
        perm(idx+1, check | (i<<j)) # 원상복구가 필요 없다.
        
perm(0, 0)
```



## 4. Swap을 이용한 순열 구하기

```python
arr = [1, 2, 3]

N = 3

def perm(idx):
    if idx == N:
        print(arr)
    else:
        for i in range(idx, N):
            arr[idx], arr[i] = arr[i], arr[idx]
            perm(idx+1)
            arr[idx], arr[i] = arr[i], arr[idx]
            
perm(0)
```



## 5. 거듭제곱 구하기

```python
# 반복문을 이용한 선형시간 O(n)

def Iterative_Power(x, n):
    result = 1
    
    for i in range(1, n + 1):
        result *= x
        
    return result

# 분할 정복을 이용한 거듭제곱 O(LogN)

def Recursive_Power(x, n):
    if n == 1:
        return x
    if n % 2 == 0:
        y = Recursive_Power(x, n // 2)
        return y * y
    else:
        y = Recursive_Power(x, (n - 1) // 2)
        return y * y * x
```



