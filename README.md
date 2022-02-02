
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
