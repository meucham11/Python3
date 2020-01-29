### enumerate
```text
list의 element를 추출할 때 번호를 붙여서 추출한다.
```

```python3
# i에는 인덱스  v에는 값
for i, v in enumerate(['tic','tac','toc']):
    print(i, v)
    
    
mylist = ['a','b','c','d']
list(enumerate(mylist))   


{i:j for i,j in enumerate('Hi my name is meucham'.split())}


```


### zip
```text
n개의 list의 값을 병렬적으로 추출함 (각 리스트에서 1번째인덱스 위치에 있는 것을 가져옴, 그다음 각리스트의 2번째 ...)
```

```python3
a,b,c=zip((1,2,3),(10,20,30),(100,200,300))
a
b
c

[x for x in zip(zip((1,2,3),(10,20,30),(100,200,300)))]
[sum(x) for x in zip(zip((1,2,3),(10,20,30),(100,200,300)))]
```

```python3
for i, (a,b) in enumerate(zip(alist,blist)):
    print(i,a,b)
```
