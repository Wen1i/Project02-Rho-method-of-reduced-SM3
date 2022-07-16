# Rho-method-of-reduced-SM3
## 关键代码
~~~
def Rho(n):
    x = random.random()
    h1 = SM3(str(x))
    h2 = SM3(str(h1))
    while 1:
        h1 = SM3(str(h1))
        h2 = SM3(str(SM3(h2)))
        if h1[:n] == h2[:n]:
            break
    return (h1[:n], h2[:n])
~~~
