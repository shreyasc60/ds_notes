--------------------------------------------------------------------------
Notes taken while following along the Google Data Analytics course from Coursera.

## 1. Functions used in this tutorial

1. separate()
2. unite()
3. mutate()

#### 1.1 separate()

**Separate a character column into multiple columns** with a regular expression or numeric locations

```r
# e.g
employee |> separate(full_name, into = c("first_name", "last_name"), sep = " ")
```

Output:
```
id         full_name    job_title
1          John Mendes Professional
2          Rob Stewart   Programmer
3    Rachel Abrahamson   Management
4      Christy Hickman     Clerical
5       Johnson Harper    Developer
6       Candace Miller   Programmer
7        Carlson Landy   Management
8         Pansy Jordan     Clerical
9         Darius Berry    Developer
10     Claudia Garcia   Programmer
```

#### 1.2 unite()

It is the **complement of separate()** function. It is a convenience function to **paste multiple columns into one**.

```r
# e.g
employee_2 |> unite("full_name", first_name, last_name, sep = " ")
```

Output:
```
 id         full_name    job_title
1          John Mendes Professional
2          Rob Stewart   Programmer
3    Rachel Abrahamson   Management
4      Christy Hickman     Clerical
5       Johnson Harper    Developer
6       Candace Miller   Programmer
7        Carlson Landy   Management
8         Pansy Jordan     Clerical
9         Darius Berry    Developer
10     Claudia Garcia   Programmer
```

#### 1.3 mutate()

`mutate()` **creates new columns** that are functions of existing variables. It can also **modify** (if the name is the same as an existing column) and **delete columns** (by setting their value to `NULL`).

```r
# e.g
library(palmerpenguins)
penguins |> mutate(body_mass_kg = body_mass_g/1000) |> select(body_mass_kg)
```

Output:
```
# A tibble: 344 × 1
   body_mass_kg
          <dbl>
 1         3.75 2         3.8 3         3.25 4        NA   
 5         3.45 6         3.65 7         3.62 8         4.68 9         3.48
10         4.25
# ℹ 334 more rows
# ℹ Use `print(n = ...)` to see more rows
```