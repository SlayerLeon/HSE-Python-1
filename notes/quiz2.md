### Quiz 2 :thought_balloon:


* __A. Голосование__

```python
# (0 + 0 + 0) // 2 = 0
# (0 + 0 + 1) // 2 = 0
# (0 + 1 + 1) // 2 = 1
# (1 + 1 + 1) // 2 = 1

def Election(x, y, z):
    return (x + y + z) // 2

a = list(map(int, input().split()))
print(Election(a[0], a[1], a[2]))

```

* __C. Сумма произведений соседних чисел__

```python
# n = 4
# 1*2+2*3+3*4=20

n = int(input())

c = 0
a = []

for i in range(1, n):
    c += i * (i + 1)
    a.append(str(i) + '*' + str(i + 1))

print('+'.join(a) + '=' + str(c))


 ```
* __D. Таблица умножения - 2__
```python
m1, m2 = list(map(int, input().split()))
n1, n2 = list(map(int, input().split()))

for i in range(m1, m2 + 1):
    for j in range(n1, n2 + 1):
        print(str(i) + ' x ' + str(j) + ' = ' + str(i * j))
    print()
```
* __E. Треугольники__
```python
n = int(input())
a = list(map(int, input().split()))


def isOK(a, b, c):
    if a + b > c and a + c > b and b + c > a:
        return True
    return False


ans = 0
for i in range(n - 2):
    for j in range(i + 1, n - 1):
        for k in range(j + 1, n):
            if isOK(a[i], a[j], a[k]):
                ans += 1

print(ans)
```

* __G. Количество цифр__

```python
a = [0] * 9

while True:
    x = int(input())
    if x == 0:
        break
    a[x - 1] += 1
    
print(*a)
```
* __H. Чемпионат по метанию коровьих лепешек__

```python
n = int(input())
a = list(map(int, input().split()))

mx = max(a)
idx_max = 0

for i in range(n):
    if a[i] == mx:
        idx_max = i
        break

possible = []

for i in range(idx_max + 1, n - 1):
    if str(a[i])[-1] == '5' and a[i + 1] < a[i]:
        possible.append(a[i])

if len(possible) == 0:
    print(0)
else:
    vasya = max(possible)
    a.sort(reverse=True)
    for i in range(n):
        if a[i] == vasya:
            print(i + 1)
            break


```


* __B. Ханойские башни__ [Solution](https://www.youtube.com/watch?v=rFuQCd4RvI0)
<p align="center">
  <img width="400" height="200" src="http://alexandrsoldatkin.com/c-hanoi-tower/images/towershanoi.jpg">
</p>

```python
def move(n, a, b):
    if n <= 0:
        return None
    move(n - 1, a, 6 - a - b)
    print(n, a, b)
    move(n - 1, 6 - a - b, b)

n = int(input())

a = 1

if n % 2 == 0:
    b = 3
else:
    b = 2

for k in range(n, 0, -1):
    move(k, a, b)
    if k % 2 == 1:
        a = 2
        b = 3
    else:
        a = 3
        b = 2
```
* __F. Жизнь в квадрате__

```python
import copy

n, t = list(map(int, input().split()))

a = []
for i in range(n):
    a.append(list(map(int, input().split())))


def inSqare(i, j):
    if 0 <= i < n and 0 <= j < n:
        return True
    return False


def count(i, j):
    c = 0
    for x in range(-1, 2, 1):  # -1 0 1
        for y in range(-1, 2, 1):  # -1 0 1
            if x == 0 and y == 0:
                continue
            if inSqare(i + x, j + y) and a[i + x][j + y] == 1:
                c += 1
    return c


def next():
    b = copy.deepcopy(a)
    for i in range(n):
        for j in range(n):
            if a[i][j] == 1:
                if 2 <= count(i, j) <= 3:
                    b[i][j] = 1
                else:
                    b[i][j] = 0
            else:
                if count(i, j) == 3:
                    b[i][j] = 1
    return b


for i in range(t):
    a = next()

for i in range(n):
    print(*a[i])
```
