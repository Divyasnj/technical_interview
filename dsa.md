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

### sum of the digits
```
def sumOfDigits(self, n):
        # code here
        sum=0
        while n>0:
            ld=n%10
            sum+=ld
            n=n//10
        return sum
```

### Reverse the Number
```
def reverseDigits(self, n):
		# Code here
		rev=0
		while n>0:
		    ld=n%10
		    rev=rev*10+ld
		    n=n//10
	    return rev
```

### palindrome number
```
def isPalindrome(self, n):
		# code here
		rev=0
		k=n
		while n>0:
		    ld=n%10
		    rev=rev*10+ld
		    n=n//10
	    if k==rev:
	        return True
	    else:
	        return False
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

k="madam"
print(palin(k))
```


### count vowels in string..
```
k=['a','e','i','o','u']
s="divyA"
s=s.lower()
v=0
for i in range(len(s)):
    if s[i] in k:
       v+=1
print(v)
```

### Armstrong number
```
def armstrongNumber (self, n):
        k=n
        total=0
        # code here
        while n>0:
           ld=n%10
           total+=ld**3
           n=n//10
        if k==total:
            return True
        else:
            return False
```


