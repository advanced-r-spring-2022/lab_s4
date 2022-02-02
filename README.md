
<!-- README.md is generated from README.Rmd. Please edit that file -->

# cdouble: Cached Doubles

<!-- badges: start -->
<!-- badges: end -->

Build an R package that provides definitions and methods for an S4 class
called `cdouble` that caches the total sum of the double in a slot.

-   The `cdouble` class should inherit from the `double` type.
-   The `cdouble` class should have slots:
    -   `.Data`: This is the implicit slot inherited from the double
        type.
    -   `s`: This is the sum of the double elements.
-   Create a generic and method to get `s`.
-   Create a helper function to create a `cdouble` object from just a
    `double` vector.
-   Create a `show()` method
-   Create methods to perform arithmetic operations on two objects of
    class `cdouble`, where the sum is updated when these operations are
    complete.
-   Create methods to perform subsetting operations on `cdouble`
    objects.
-   Make sure you document the `cdouble` class, all methods, and all
    generics.

# Example Usage

``` r
library(cdouble)
```

-   Easy to define `cdouble` objects:

    ``` r
    x <- cdouble(c(1, 3, 5))
    ```

-   Nice printing:

    ``` r
    x
    #> value: 1 3 5 
    #>   sum: 9
    ```

-   Arithmetic operations work between `cdouble` objects.

    ``` r
    y <- cdouble(c(2, 4, 6))
    x + y
    #> value: 3 7 11 
    #>   sum: 21
    x / y
    #> value: 0.5 0.75 0.8333 
    #>   sum: 2.083
    x - y
    #> value: -1 -1 -1 
    #>   sum: -3
    x * y
    #> value: 2 12 30 
    #>   sum: 44
    ```

-   Arithmetic operations work between `cdouble` objects and `double`s.

    ``` r
    x + 2
    #> value: 3 5 7 
    #>   sum: 15
    x - 2
    #> value: -1 1 3 
    #>   sum: 3
    x / 2
    #> value: 0.5 1.5 2.5 
    #>   sum: 4.5
    x * 2
    #> value: 2 6 10 
    #>   sum: 18
    ```
