```python3
result1 = []
for i in range(10):
  result.append(i)
result1


result2 = [i for i in range(10)]


result3 = [i for i in range(10) if i % 2==0]

```
---
```python3
 # 1차원으로 출력
word_1='hello'
word_2='world'
result = [i+j for i in word_1 for j in word_2] 


case_1=['A','B','C']
case_2=['D','E','F']

result = [i+j for i in case_1 for j in case_2 if not(i==j)]

```

```python3

# 2차원 리스트로 출력
case_1=['A','B','C']
case_2=['D','E','F']
result1 = [[i+j for i in case_1] for j in case_2]



words = 'The quick brown fox jumps over the lazy dog'.split()

result2 = [[w.upper(), w.lower(), len(w)] for w in words]

```

```python3


```

```python3


```

```python3


```

```python3


```

```python3


```

```python3


```
