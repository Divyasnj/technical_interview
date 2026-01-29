```
def todig(n,a):
    if n==0:
        return
    dig=n%10
    n=n//10
    todig(n,a)
    print(a[dig],end=" ")
    
a=["zero","one","two","three","four","five","six","seven","eight","nine"]
n=145
todig(n,a)
```

