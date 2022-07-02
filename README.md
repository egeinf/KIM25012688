# КИМ № 25012688 БР № 2832503195017 

![image](https://user-images.githubusercontent.com/70198995/176993350-1fe87ddc-b1ea-4e1d-8f6d-77829828fb06.png)

![image](https://user-images.githubusercontent.com/70198995/176993364-07f93a54-b48f-4a09-a901-3cfe87bb7dd7.png)

![image](https://user-images.githubusercontent.com/70198995/176993030-42fe9b20-5d52-45f6-b0bc-9504579fd13b.png)

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
