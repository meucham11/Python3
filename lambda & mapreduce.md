## lambda
```text
함수 이름 없이, 함수처럼 쓸 수 있는 익명 함수

lambda x,y: x+y
```

## map
```text
sequence 자료형 각 element에 동일한 함수를 적용함

map(function,list_data)


ex=[1,2,3,4,5]
ez=[10,20,30,40,50]
list(map(lambda x: x**2,ex))
list(map(lambda x,y:x+y,ex,ez))

list(map(lambda x: x**2 if x%2==0 else x,ex))  # else가 필수다.
>>> 
```

## reduce
```text
누적의 느낌
```
```python3
from functools import reduce
reduce(lambda x,y: x+y, ex)


def fac(n):
    return reduce(lambda x,y : x*y, range(1,n+1))
    
fac(5)
```
