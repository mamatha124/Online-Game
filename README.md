# Online-Game in python
n = int(input())
a = list(map(int, input().split()))[:n]
p1 = 0
p2 = n - 1
while p1 < p2:
    while a[p1] % 2 == 0 and p1 < p2:
        p1 += 1
    while a[p2] % 2 != 0 and p1 < p2:
        p2 -= 1
    if p1 < p2:
        a[p1], a[p2] = a[p2], a[p1]
        p1 += 1
        p2 -= 1
print("Array after Segregation")
print(*a)
