### no in words with space..
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
### palindrome string
```
def palin(k):
    n=len(k)
    left=0
    right=n-1
    while left<right:
       if k[left]!=k[right]:
           return False
       left+=1
       right-=1
    return True
```
k="madam"
print(palin(k))
