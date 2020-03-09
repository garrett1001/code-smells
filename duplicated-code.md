### Duplicated Code!

#### How to recognize Duplicated Code

When two sections or functions do the same thing, it is code duplication. Some algorithms to detect code duplication are: Baker's algorithm, Rabin–Karp string search algorithm. Using Abstract Syntax Trees, Visual clone detection, count Matrix Clone Detection, Locality-sensitive hashing, and Anti-unification.

#### Duplicated Code example:

[Sourced From Wikipedia](https://en.wikipedia.org/wiki/Duplicate_code)
```c++
extern int array_a[];
extern int array_b[];
 
int sum_a = 0;

for (int i = 0; i < 4; i++)
   sum_a += array_a[i];

int average_a = sum_a / 4;
 
int sum_b = 0;

for (int i = 0; i < 4; i++)
   sum_b += array_b[i];

int average_b = sum_b / 4;
```
