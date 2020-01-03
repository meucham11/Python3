import matplotlib.pyplot as plt

## 기타 설정
### 선명하게 보기
from IPython.display import set_matplotlib_formats

### 한글깨짐 -깨짐 방지  
```
첫번째 방법(window)
from matplotlib import font_manager, rc

 

import matplotlib

 

font_name = font_manager.FontProperties(fname="c:/Windows/Fonts/malgun.ttf").get_name()

rc('font', family=font_name)

matplotlib.rcParams['axes.unicode_minus'] = False
```

```
두번째 방법(window, mac)
import matplotlib
import seaborn as sns

# Windows
# matplotlib.rc('fon', family="NanumGothic")
# matplotlib.rc('fon', family="Malgun Gothic")

# Mac
# matplotlib.rc('fon', family="AppleGothic")
```

## 창 갯수
```figure, ax = plt.subplots(nrows=1, ncols=1)```

## 창 크기
```
### inch
figure.set_size_inches(18, 4)
### cm
plt.figure(figsize=(10,5))

```

## lim
```plt.ylim(0, 1)```


