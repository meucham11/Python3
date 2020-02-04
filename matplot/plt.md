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
figure, axex = plt.subplots(nrows=?, ncols=?)
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
