--------------------------------------------------------------------------
### Vectors
Vectors are of two types
1. Atomic Vectors
2. Lists

![Vectors Summary](summary-tree.png)
In atomic vectors all the elements are of the same type, whereas in lists data elements can be of different types. 

### Atomic Vectors
![Atomic Vectors Summary](summary-tree-atomic.png)
We can use the c() or the combine function to create a vector.

```r
# to create a vector of integers
x <- c(1L, 2L, 3L, 4L, 5L)
# to create a vector of a range of integers
x <- c(1:500)
# to create a vector of strings, doubles, and logical values respectively
x <- c("hello", "world")
x <- c(2.3, 2.4, 5.6)
x <- c(TRUE, FALSE, TRUE, TRUE)

```
