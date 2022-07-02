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
# 6
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


![image](https://user-images.githubusercontent.com/70198995/176993030-42fe9b20-5d52-45f6-b0bc-9504579fd13b.png)
