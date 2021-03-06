# 재귀함수(Recursive Function)

재귀함수란, 자기 자신을 다시 호출하는 함수를 의미한다.

```python
def recursive_function():
    print('재귀함수 호출')
    recursive_function()

recursive_function()
```

'재귀함수 호출' 문자열을 무한히 출력.
어느정도 출력하다가 최대 재귀 깊이 초과 메세지가 출력된다.

```
RecursionError: maximum recursion depth exceeded while calling a Python object
재귀함수 호출
```

재귀함수는 DFS를 구현할 때 자주 쓰이게 된다.

## 재귀함수의 종료조건

재귀함수를 문제 풀이에서 사용할 때는 재귀함수의 종료 조건을 반드시 명시해야 한다.

종료 조건을 제대로 명시하지 않으면(위와 같이) 함수가 무한히 호출 될 수 있다.

```python
def recursive_function(i):
    # 100번째 호출을 했을 때 종료되도록 종료 조건 명시
    if i ==100:
        return
    print(i,"번째 함수에서",i+1,'재귀함수 호출합니다')
    recursive_function(i + 1)
    print(i,"번째 재귀함수를 종료합니다.")
recursive_function(1)

```

```python
def gcd(a,b):
    if a % b == 0:
        return b
    else:
        return gcd(b, a%b)

print(gcd(192,162))
```

## 재귀함수 사용의 유의 사항

재귀함수를 잘 활용하면 복잡한 알고리즘을 간결하게 작성할 수 있다.  
컴퓨터가 함수를 연속적으로 호출하면 컴퓨터 메모리 내부의 스택 프레임에 쌓인다.  
그래서 스택을 사용해야 할 때, 구현상 스택 라이브러리 대신에 재귀함수를 이용하는 경우가 많다.
