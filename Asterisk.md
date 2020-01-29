## Asterisk 가변인자,키워드인자, unpacking 
```text
쉽게 이해하자면 매개변수에 *이 있으면 묶어주기
변수 앞에 있으면 unpacking

**은 dict에 쓰는 거
```
```python3
# 가변인자
def asterisk_test(a, *args):
    print(a, args)
    print(type(args))

asterisk_test(1,2,3,4,5,6)    # 1은 a로 들어가고 2,3,4,5,6은 tuple형태로 *args로 들어간다.
```

```python3
# 키워드인자
def asterisk_test(a, **kargs):
    print(a, kargs)
    print(type(kargs))

asterisk_test(1, b=2, c=3, d=4, e=5, f=6)  # 1은 a로 들어가고 2,3,4,5,6은 dict형태로 *args로 들어간다.
```


```python3
def asterisk_test(a, *args):
    print(a, args[0])
    print(type(args))

asterisk_test(1, (2, 3, 4, 5, 6))
```


```python3
[data for data in zip(*([1,2],[3,4],[5,6]))]


data = {"d":1 , "c":2, "b":3, "f"=56}
asterisk_test(10, **data)

```
