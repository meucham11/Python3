# class : 현실세계의 물건(object)을 만들어 보자.
```python3
class Car:
    man=4
    tire=4
    def run(self):  # self는 필수
        # 코드 작성
        pass
    
    def stop(self):
        # 코드 작성
        pass
    
    
c1=Car()
c2=Car()
c3=Car()
```

# 생성자
```python3
def __init__(self):
    code
```
# 소멸자
### 프로그램이 종료되면 돌아가는 함수
```python3
def __del__(self):
    code
```
---
---
```python3
# 생성자, 소멸자, 디폴트 매개변수
class Car:
    man = 4
        
c1=Car()
c2=Car()   

## 자동차를 만들때 man은 4로 정해진다.   c1.man=6 으로 바꿀수 있긴함
## 하지만 객체를 만들과 동시에 뭔가를 바꾸고 싶다 하면 생성자를 이용한다.
class Car:
    man=4
    
    def __init__(self,_man=4):
        self.man=_man
    
    
c1=Car()  # 생성자에서 default는 4
c1.man
c2=Car(6) # 생성자에서 값을 받으면 6
c2.man
```

---
---

# 상속
```
부모의 모든 것을 물려 받는것.
부모의 돈도 내돈, 내돈도 내돈.
```
```python3
class t1:
    i=1
    def test(self):
        print('test')
class t2(t1):
    j=2
    def test(self):
        pass
        
c1=t1()    # i만
c1.test()
c1.i
c2=t2()    # i와 j 존재
```
```python3
class t1:
    i=1
    def test(self):
        pass
    def __init__(self,_i=4):
        self.i=_i
        
class t2(t1):
    j=2
    def test(self):
       pass 
    
    def __init__(self,_i=1,_j=2):
        #self.i=_i   # 여기서 i를 지정하기보단 부모 클래스에서 i를 지정하는게 안정적이다.
        super().__init__(_i) ## 그래서 부모 생성자를 여기서 불러낸다. 이 루틴을 꼭 넣어주자. 
                              #호출이기 때문에 self를 넣지 않는 것이다.
        self.j=_j
        
c1 = t1(9)
print(c1.i)
c2 = t2(12,14)
print(c2.i, c2.j)

t2.test
```



# 연산자 오버로딩
```python3
class T1:
    i=4
    def __add__(self, other): # self가 c1 // other가 c2 가 된다.
        temp=T1()
        temp.i=self.i+other.j+5
        return temp
    def test(self):
        print('test')
        
class T2(T1):
    j=2
    def test(self):
        print('T2 test')
        
c1=T1()
c2=T2()

c3=c1+c2
print(c3.i) 
print(c1.i, c2.i, c2.j) # 변화없음을 확인할 수 있다.
```




# 연산자 오버라이딩
```
t2가 t1을 상속 받을 때 위의 예제들 처럼 test 같이 함수 이름이 같을 때 자식의 객체를 생성하면 
t2의 test가 t1의 test 위에서 작동한다. 즉 t1의 test는 작동을 안하는 것이다.

굳이 t1의 test를 돌리고 싶으면 t2 클래스 test 함수 안에
super().test()  <- t1의 test 작동
code <- t2 test 작동 내용을 작성하면 된다.


class T1:
    i=4
    def __add__(self, other): # self가 c1 // other가 c2 가 된다.
        temp=T1()
        temp.i=self.i+other.j+5
        return temp
    def test(self):
        print('test')
        
class T2(T1):
    j=2
    def test(self):
        super().test()
        print('T2 test')
        
t1=T1()
t2=T2()

t1.test()
t2.test()

```
