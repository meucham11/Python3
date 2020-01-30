```python3
import numpy as np


### shape
# -1을 하면 미지정이라는 뜻 뒤에 3이 기준이되서 3열로 맞춰준다.
a=np.array([1,4,5,8,6,3,9,7,2],int).reshape(-1,3)

# 1차원으로 펴주는거
test_m=[[[1,2,3,4],[1,2,5,8]],[[4,5,6,7],[5,6,7,8]]]
np.array(test_m)
np.array(test_m).flatten()



### slicing
test_m=np.array([[1,2,5,8],[3,4,6,8],[4,3,5,1],[9,7,6,1]])
test_m[1,1]
test_m[1][1]
test_m[:,2:]
test_m[1,:3]

'''
x:y:z
x=시작
y=끝
z=띄워라
'''
test_m[:,::2]
test_m[:,1::2]
test_m[::2,::3]



### create function
# arange
np.arange(30)
list(np.arange(30))
np.arange(30).tolist()
np.arange(30).reshape(-1,5)

np.arange(0,5,0.5)  #r의 rep

# zeros, ones
np.zeros(shape=(10,), dtype=np.int8)
np.zeros(shape=(5,5), dtype=np.int8)
np.ones(shape=(5,5), dtype=int)

# eye
np.eye(5)
np.eye(3,5,dtype=int)
np.eye(3,5,k=2)  # k는 시작인덱스 k= 생략하고 2만 써도됨





### axis
test_m=np.arange(1,13).reshape(3,4)
test_m.sum(0)
test_m.sum(1)




### concat    # concat은 np를 쓰는 것은 느리다.
a=np.array([[1,2,3]])
b=np.array([[4,5,6]])

np.hstack((a,b))
np.concatenate((a,b),axis=1)

np.vstack((a,b))
np.concatenate((a,b),axis=0)





### operation
# array간 shape이 같을 때 *   해당 위치끼리 곱
test_m=np.arange(1,13).reshape(3,4)
test_m*test_m
# 행렬 곱
test_m.dot(test_m.T)




### comparisons
# logialc_
a = np.array([1,3,0])
np.logical_and(a>0,a<3)

b= np.array([True,True,False])
np.logical_not(b)

np.logical_or(a>0,a<1)


# where 두가지 쓰임새
a=np.array([-5,0,1,4,8])  
np.where(a>1)
a[np.where(a>1)]
np.where(a>1,2,0)


# argmax argmin
a=np.array([1,2,4,8,3,4])
np.argmax(a)
b = np.arange(1,13).reshape(3,4)
np.argmax(b)
np.argmax(b,axis=0)
np.argmax(b,axis=1)

```
