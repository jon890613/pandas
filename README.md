## pandas
```
拿公投統計資料學 pandas
https://newtoypia.blogspot.com/2018/12/pandas.html
```

```

!wget https://raw.githubusercontent.com/MyDearGreatTeacher/AI_and_security_2020/master/referendum2.csv


```
## 上課筆記


Timestamp 時間戳記  


## 錯誤更正

```

更改前


df2 = pd.DataFrame({    'A': 1.,
                        'B': pd.Timestamp('20130102'),
                        'C': pd.Series(1, index=list(range(6)), dtype='float32'),
                        'D': np.array([3] * 4, dtype='int32'),
                        'E': pd.Categorical(["test", "train", "test", "train"]),
                        'F': 'foo'})



錯誤提醒   array length 4 does not match index length 6 


更改後

df2 = pd.DataFrame({'A': 1.,
                        'B': pd.Timestamp('20130102'),
                        'C': pd.Series(1, index=list(range(4)), dtype='float32'),
                        'D': np.array([3] * 4, dtype='int32'),
                        'E': pd.Categorical(["test", "train", "test", "train"]),
                        'F': 'foo'})

```
