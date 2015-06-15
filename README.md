### Usage

> c=rbind(c(1, -1/4), c(-1/4, 1))  
> m <- makeCacheMatrix(c)
> cacheSolve(m)

> [1,] 1.0666667 0.2666667
> [2,] 0.2666667 1.0666667

### Readme

Matrix inversion is usually a costly computation and there may be some
benefit to caching the inverse of a matrix rather than computing it
repeatedly (there are also alternatives to matrix inversion that we will
not discuss here). 

1.  `makeCacheMatrix`: This function creates a special "matrix" object
    that can cache its inverse.
2.  `cacheSolve`: This function computes the inverse of the special
    "matrix" returned by `makeCacheMatrix` above. If the inverse has
    already been calculated (and the matrix has not changed), then
    `cacheSolve` should retrieve the inverse from the cache.

Computing the inverse of a square matrix can be done with the `solve`
function in R. For example, if `X` is a square invertible matrix, then
`solve(X)` returns its inverse.

Assume that the matrix supplied is always
invertible.


