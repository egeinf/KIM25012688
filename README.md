# КИМ № 25012688 БР № 2832503195017 

![image](https://user-images.githubusercontent.com/70198995/176993350-1fe87ddc-b1ea-4e1d-8f6d-77829828fb06.png)

![image](https://user-images.githubusercontent.com/70198995/176993364-07f93a54-b48f-4a09-a901-3cfe87bb7dd7.png)

```python
for x in 0,1:
    for y in 0,1:
        for z in 0,1:
            for w in 0,1:
                F = not(w <= z) or (x <= y) or not (x)
                if F == 0:
                    print(w,z,y,x)
                    
# 1 X X X 
# 0 1 0 X
# X 0 X X
```

![image](https://user-images.githubusercontent.com/70198995/176993622-909204a5-3808-495c-91d3-93fa706c99cb.png)

https://github.com/egeinf/KIM25012688/raw/main/3.xlsx

![image](https://user-images.githubusercontent.com/70198995/176993777-0f7f94eb-44f3-4c53-8656-00e2f4213d6f.png)

![image](https://user-images.githubusercontent.com/70198995/176994667-a9a3e5dd-d189-410e-9d0b-8ad8a582e4fd.png)

```python
def f(x):
    x = int(x)
    res = 0
    while x:
        res += x % 10
        x //= 10
    return res
for N in range(1,9):
    res = N
    N = bin(N)[2:]
    if f(N) % 2 == 0:
        N = N + '0'
        N = '10' + N[2:]
    elif f(N) % 2 != 0:
        N = N + '1'
        N = '11' + N[2:]
    print(res, N)
# > 10000 (8)
```
### 6

```python
for s in range(1000):
    res = s
    s = (s-21) // 10
    n = 1
    while s >= 0:
        n = n * 2
        s = s - n
    if n == 8:
        print(res)
        break
```
### 7

Для хранения сжатого произвольного растрового изображения размером 640 на 256 пикселей отведено 170 Кбайт памяти без учёта размера заголовка файла. Файл оригинального изображения больше сжатого на 35%. Для кодирования цвета каждого пикселя используется одинаковое количество бит, коды пикселей записываются в файл один за другим без промежутков. Какое максимальное количество цветов можно использовать в изображении?

```python
k = 640 * 256
I = 170 * 1024 * 8 * 1.35
i = I // k
print(2**i)
```
### 8

Определите количество пятизначных чисел, записанных в восьмеричной системе счисления, в записи которых ровно одна цифра 6, при этом никакая нечётная цифра не стоит рядом с цифрой 6.

```python
k = 0
for x in range(1,99999):
    x8 = oct(x)[2:]
    if x8.count('6') == 1 and len(x8) == 5:
        if ('16' not in x8) and ('36' not in x8) and ('56' not in x8) and ('76' not in x8) and ('96' not in x8):
            if ('61' not in x8) and ('63' not in x8) and ('65' not in x8) and ('67' not in x8) and ('69' not in x8):
                k += 1
                print(x, x8, k)
```

### 11
![image](https://user-images.githubusercontent.com/70198995/176997278-5566ada6-9908-4d85-add3-d6eea9552cfe.png)

### 12
![image](https://user-images.githubusercontent.com/70198995/176997312-637c7e7a-30f7-4ed0-9e2a-7dcb4a18054e.png)

```python
s = '9' * 96
while '22222' in s or '9999' in s:
    if '22222' in s:
        s = s.replace('22222', '99', 1)
    else:
        s = s.replace('9999', '2', 1)
print(s)
```

### 14

![image](https://user-images.githubusercontent.com/70198995/176998194-f45f12d5-c4cb-4914-b4a2-c83b78a9014a.png)

```python
x = 4 * 625 ** 1920 + 4 * 125 ** 1930 - 4 * 25 ** 1940 - 3 * 5 ** 1950 - 1960
res = ''
while x:
    res = res + str(x % 5)
    x //= 5
print(res.count('0'))
```

### 15

![image](https://user-images.githubusercontent.com/70198995/176998423-a4ee6fa6-6c1b-4821-be43-c3f626a877de.png)

```python
for A in range(1,1000):
    flag = 1
    for x in range(1,1000):
        F = ( (x % 2 == 0) <= (x % 3 != 0) ) or (x+A >= 80)
        if F == 0:
            flag = 0
    if flag == 1:
        print(A)
        break
```

### 16

![image](https://user-images.githubusercontent.com/70198995/176998484-c26cd4e1-ae70-4578-9139-9383701a8755.png)

```python
def f(n):
    if n < 3: return 1
    if n % 2 == 0: return f(n-1) + n - 1
    return f(n-2) + 2*n - 2
    
print(f(34))
```

# 25
![image](https://user-images.githubusercontent.com/70198995/176999557-8070a36a-591c-4af0-83ed-8f2fd99a6799.png)

```python
for x in range(12340, 12349999):
    if x % 141 == 0:
        x = str(x)
        if x[0] == '1' and x[1] == '2' and x[2] == '3' and x[3] == '4' and x[-1] == '7':
            print(x, int(x) / 141)
```









![image](https://user-images.githubusercontent.com/70198995/176993030-42fe9b20-5d52-45f6-b0bc-9504579fd13b.png)
