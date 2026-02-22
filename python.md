🔹 append()
👉 Adds one single element to the list (even if that element is another list).
```
a = [1, 2, 3]
a.append([4, 5])

print(a)
# [1, 2, 3, [4, 5]]
```

🔹 extend()
👉 Adds each element of another iterable to the list.
```a = [1, 2, 3]
a.extend([4, 5])

print(a)
# [1, 2, 3, 4, 5]
```



### shallow copy and deep copy
1️⃣ First Important Concept: Python Variables are References
In Python, variables do not store values
They store addresses (references) to objects in memory
a = [1,2,3]
b = a

Now:
a ----\
       ----> [1,2,3]   (same object)
b ----/

So if you change b, a also changes.
b[0] = 100
print(a)   # [100,2,3]

Because both point to same memory

2️⃣ Why Copy is Needed?
When data is nested (list inside list, dict inside dict), we sometimes want a real independent duplicate
Python provides:
import copy
copy.copy()      -> Shallow Copy
copy.deepcopy()  -> Deep Copy


3️⃣ Shallow Copy (copy.copy())
👉 Copies only the OUTER object
👉 Inner objects are still shared
Memory Diagram
Original list:
a = [[1,2,3], [4,5,6]]

After shallow copy:
a  ------>  [ L1 , L2 ]
              |     |
b  ------>  [  |     | ]
              ↓     ↓
            [1,2,3] [4,5,6]

Outer list is new
Inner lists are SAME

Example
import copy

a = [[1,2,3],[4,5,6]]
b = copy.copy(a)

b[0][0] = 99

print("a:",a)
print("b:",b)

Output
a: [[99, 2, 3], [4, 5, 6]]
b: [[99, 2, 3], [4, 5, 6]]

🔴 Change reflected in original
Why?
Because inner lists are shared

4️⃣ Deep Copy (copy.deepcopy())
👉 Copies EVERYTHING recursively
👉 Completely independent object
Memory Diagram
a  ------>  [ L1 , L2 ]
              |     |
              ↓     ↓
            [1,2,3] [4,5,6]

b  ------>  [ L3 , L4 ]
              |     |
              ↓     ↓
            [1,2,3] [4,5,6]

Now NO shared memory

Example
import copy

a = [[1,2,3],[4,5,6]]
b = copy.deepcopy(a)

b[0][0] = 99

print("a:",a)
print("b:",b)

Output
a: [[1, 2, 3], [4, 5, 6]]
b: [[99, 2, 3], [4, 5, 6]]

🟢 Original unchanged

5️⃣ Key Difference (INTERVIEW TABLE ⭐)
FeatureShallow CopyDeep CopyFunctioncopy.copy()copy.deepcopy()Outer objectNewNewInner objectsSharedCopiedMemory usageLowHighSpeedFasterSlowerSafe for nested objects❌ No✅ YesChanges affect originalSometimesNever

6️⃣ One-Line Interview Answer 🎯

Shallow copy duplicates only the top-level object and shares nested objects, whereas deep copy recursively duplicates all objects, creating a completely independent copy.
