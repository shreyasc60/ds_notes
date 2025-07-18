--------------------------------------------------------------------------
## 1. Libraries required
#### 1.1 We can use the following packages for cleaning data in R:
1. Here
2. Skimr
3. Janitor

#### 1.2 Installing and importing libraries
**The here package makes referencing files easier**. It can be installed using the following command:
```r
install.packages("here")
library(here) #load the library
```

**The skimr package helps you summarize and skim through data quickly.**
```r
install.packages("skimr")
library(skimr)
```
**The janitor package has various functions for cleaning data.**
```r
install.packages("janitor")
library(janitor)
```

**Note**: You could, of course, install all these packages in one single line using the **c()** combine function. Here's how it's done:
```r
install.packages(c("here", "skimr", "janitor"))
```

We also need to load the dplyr package as we'll be using some of it's functions in the process.
```r
library(dplyr)
```

## 2. Importing the data

You can either import your data using the **read_csv()** function from the readr package, or you could work on an in-built dataset, like **palmerpenguins** for example. 

```r
# This dataset can be installed and loaded as follows
install.packages("palmerpenguins")
library(palmerpenguins)
```

The dataset or a tibble of it's preview can be accessed using:
```r
penguins
```

## 3. Summarizing data

We can use the **skim_without_charts()** function from the **skimr** package, to obtain a comprehensive data summary of our dataset.

```r
# e.g
skim_without_charts(penguins)
# or
skimr::skim_without_charts(penguins)
```

Or, we could use the **glimpse()** function from the **dplyr** package.
```r
glimpse(penguins)
```

To obtain the preview of first few rows of the dataset, we can use the **head()** function. It returns the top 6 rows by default, but we can use it to obtain N number of rows by passing an argument.

## 4. Commonly performed cleaning tasks

Now we'll go through some commonly performed cleaning tasks, and how we can execute them in R.

#### 4.1 Dropping columns

We might want to drop a single column, or multiple columns from our dataset. We can do this using the **select()** function from **dplyr** package. This function only selects the columns that we specify. Using **arguments** like **starts_with() or ends_with()** we can also select specific columns that start with a prefix, or end with a suffix, respectively. 

```r
# e.g Dropping the species column from penguins
# we pass the negation of species as a parameter to the select function
# so it selects all the other variables, except for species
penguins |> select(-species) 

# Or, we could use ! for negation
penguins |> select(!species)
```

We can also combine various variable with **c()** and drop multiple columns in one go.

```r
# dropping species and island variable
penguins |> select(!c(species, island))
```

#### 4.2 Renaming columns

We can use the **rename()** function to do this. Let's see an example for renaming multiple columns at once:

```r
penguins |> rename(new_species = species, new_island = island)
```

To **rename all the columns at once**, we can use the **rename_with()** function. This comes handy in situations where all the variable are in Uppercase, and we want to rename them all in lowercase. We can do this using:

```r
rename_with(penguins, tolower)
```

And now, all the variable will become lowercase. 

**Note**:
We can also use a function to automatically clean all the dirty variable names, using the **clean_names()** function from the **Janitor** package. This function ensure all the variables have unique, and consistent names.

```r
penguins |> clean_names()
```

