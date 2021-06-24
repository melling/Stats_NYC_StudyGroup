## Set up Google Drive for use in Colab

- https://drive.google.com

### Code to be placed in Jupyter Cell
```python
from google.colab import drive
drive.mount(‘/content/gdrive’)
```

### View the Files in Mounted Drive

```python
! ls gdrive/MyDrive/
```

## Discussed Discrete Distributions

Discussion based on Chapter 2 of ThinkStats: https://greenteapress.com/thinkstats2/html/thinkstats2003.html

```
[1, 2, 3, 5, 5, 9, 10, 22, 22, 15,15,15, 15, 15, 15, 15, 15, 9, 9]
```
Let's ask some questions about this distribution.

- How many times does 15 occur? 8
- How many times does 6 occur?  0
- What are all the distinct values in the list? [1, 2, 3, 5, 9, 10, 22, 15]

### Use Python to Find Answers

```python
from collections import Counter

discrete01 = [1, 2, 3, 5, 5, 9, 10, 22, 22, 15,15,15, 15, 15, 15, 15, 15, 9, 9]

cnt = Counter(discrete01)

cnt.get(15) # 15 occurs ...

cnt.get(6) # 6 occurs 0 times

cnt.keys() # dict_keys([1, 2, 3, 5, 9, 10, 22, 15])
```

### Plot a Histogram

We didn't get this to work with the Counter class.

```python
import matplotlib.pyplot as plt

#dict1 = dict(cnt)

plt.hist(discrete01, bins=25)
plt.show();
```
