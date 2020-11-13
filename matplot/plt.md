일반적인 설정
import matplotlib
## 기타 설정
### 선명하게 보기
```PYTHON3
from IPython.display import set_matplotlib_formats
```

### 한글깨짐 -깨짐 방지  
#### 첫번째 방법(window)
```PYTHON3
from matplotlib import font_manager, rc
import matplotlib

font_name = font_manager.FontProperties(fname="c:/Windows/Fonts/malgun.ttf").get_name()
rc('font', family=font_name)
matplotlib.rcParams['axes.unicode_minus'] = False
```
    
    
    
#### 두번째 방법(window,mac)
```PYTHON3
import matplotlib
import seaborn as sns

# Windows
matplotlib.rc('font', family="NanumGothic")
matplotlib.rc('font', family="Malgun Gothic")

# Mac
matplotlib.rc('font', family="AppleGothic")
```


사이즈, 창 갯수 등은 import matplotlib.pyplot as plt
## 창 갯수
```PYTHON3
figure, axes = plt.subplots(nrows=?, ncols=?)
axes[3][1]등으로 

plt.tight_layout()  # 간격 조정
ax1.set(ylabel='Count',title="연도별 대여량")
```

## 창 크기
```PYTHON3
### inch
figure.set_size_inches(18, 4)
### cm
plt.figure(figsize=(10,5))

```

## lim
```PYTHON3
plt.ylim(0, 1)
```

### sns에서 x 축 기울기
```python3
plt.xticks(rotation=30,ha='right')
```

### x축 마음대로 지정하기
## sns.lineplot   및  plot 다 가능
포인트는 x를 str로 바꾸는것
```python3
test.index=list(test['weeknum'])
result=test.loc[list(test_env['weeknum'].unique())].reset_index(drop=True)
result['weeknum']=result['weeknum'].astype(str)

fig, ax = plt.subplots(1,1)
ax.plot(result['weeknum'], result["내부온도"])
ax.set_xticklabels(result.weeknum)
plt.show()
```

![q1](https://user-images.githubusercontent.com/34879309/99043760-1031ef80-25d2-11eb-8880-485231f7e166.PNG)
![q2](https://user-images.githubusercontent.com/34879309/99043762-10ca8600-25d2-11eb-92f9-a0dcf2375c72.PNG)
</br>

## sns.boxplot
```python3
sns.boxplot(data=env_data,x='WeekNum',y=env,order=env_data['WeekNum'].unique())
```


### 여러개 그리기
```python3

plt.figure(figsize=[15,25])
plt.subplots_adjust(left = 0, bottom = 0, right = 1, top = 1, hspace = 1, wspace = 0.5)
cols = 3
rows = 13 

for i in range(1,38):
    #
    plt.subplot(rows, cols, i)
    plt.title(cat[i-1])  
    df_cat=psm[psm['CLAC1_NM']==cat[i-1]]
    sns.countplot(data=df_cat,x='month')

plt.show()
```
