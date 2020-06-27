# 爬山演算法介紹
爬山法（climbing method）是一種優化演算法，其一般從一個隨機的解開始，然後逐步找到一個最優解（區域性最優)。

```
def hillClimbing(f, x, dx=0.01):
    while (True):
        print('x={0:.3f} f(x)={1:.3f}'.format(x, f(x)))
        if f(x+dx)>f(x):
            x = x + dx
        elif f(x-dx)>f(x):
            x = x - dx
        else:
            break
    return x

def f(x):
    return -1*(x*x+3*x+5)

hillClimbing(f, 0)
```

程式為上課網站的老師範例 

參考資料:
- [上課網站](https://misavo.com/blog/%E9%99%B3%E9%8D%BE%E8%AA%A0/%E6%9B%B8%E7%B1%8D/%E4%BA%BA%E5%B7%A5%E6%99%BA%E6%85%A7/02-%E7%88%AC%E5%B1%B1%E6%BC%94%E7%AE%97%E6%B3%95)
