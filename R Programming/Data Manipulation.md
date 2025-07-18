You can use - or desc() to arrange a column in descending order using the **arrange()** function.

```r
library(tidyverse)

x <- c(1L, 2L, 3L, 4L, 5L)
y <- c(0.0, 2.3, 1.4, 0, 9.9)
df <- data.frame(x, y)

df |> arrange(-y) # arranges y in desc order
# OR
df |> arrange(desc(y)) # arranges y in desc order
```

Output:
```
  x   y
1 5 9.9
2 2 2.3
3 3 1.4
4 1 0.0
5 4 0.0
```
