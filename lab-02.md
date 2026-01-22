Lab 02 - Plastic waste
================
Rachel Weiner
January 22, 2026

## Load packages and data

``` r
library(tidyverse) 
```

``` r
plastic_waste <- read.csv("data/plastic-waste.csv")
```

## Exercises

### Exercise 1

Histograms of plastic waste per capita, faceted by continent:

``` r
ggplot(data = plastic_waste, aes(x = plastic_waste_per_cap)) +
  geom_histogram(binwidth = 0.2) + 
  facet_wrap(~ continent)
```

    ## Warning: Removed 51 rows containing non-finite outside the scale range
    ## (`stat_bin()`).

![](lab-02_files/figure-gfm/unnamed-chunk-1-1.png)<!-- --> The six
histograms above help us to visualize plastic waste per capita across
the six respective continents. It seems that Oceania and South America
has the lowest plastic waste per capita compared to the other continents
while Africa, Asia, Europe, and North American seem to have greater
plastic waste per capita.

### Exercise 2

Density curves!

``` r
ggplot(
  data = plastic_waste,
  mapping = aes(
    x = plastic_waste_per_cap,
    color = continent,
    fill = continent
  )
) +
  geom_density(alpha = 0.1)
```

    ## Warning: Removed 51 rows containing non-finite outside the scale range
    ## (`stat_density()`).

![](lab-02_files/figure-gfm/plastic-waste-density-1.png)<!-- --> This
density curve allows us to visualize plastic waste per capita in a
color-coded format. As far as the code goes, we define color and fill
within the mapping aesthetics as this helps tell r which variables we
want to display from the larger data set. On the other hand, we define
the aplha level within the plotting geom as this does not pertain to the
data itself but instead to the formatting of the plot, seperate from any
data implications.

### Exercise 3

Remove this text, and add your answer for Exercise 3 here.

``` r
# insert code here
```

### Exercise 4

Remove this text, and add your answer for Exercise 4 here.

``` r
# insert code here
```

``` r
# insert code here
```

``` r
# insert code here
```

``` r
# insert code here
```

### Exercise 5

Remove this text, and add your answer for Exercise 5 here.

``` r
# insert code here
```
