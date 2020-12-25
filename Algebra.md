# Algebra 
is an arithmatic that includes non-numerical entities.
           like 2x+5 = 25

If it has exponential term, then it isn't linear algebra.

Used in solving for unknowns within system of linear equation.

## Number of solutions of an linear equation
1. One solution : haveing differnt slope and offset (intercept)
2. Infinite solution : same slope and offset
3. No-Solution : same slope with different offset.

In ML , generally we have case with many unknowns and many equations.

## Contemporary application of Algebra
1. Solving for unknowns in ML algos.
2. Reducing dimensionality
3. Ranking results (eigen vectors)
4. Recommendations(Singular vaue decomposition, SVD)
5. NLP (e.g. SVD, Matrix factorization)

## Tensor
Fundamental building blocks of Algebra in ML. They are ML generalization of vectors and matrices to any number of dimensions.

* Scalar  : Zero dimensional tensor
           - No dimension
           - Single number
           - Should be typed like other tensor
 
 * Vector Tensor :
           - One dimensional array of numbers
           - Each element in vector is a scalar
 
 * Matrics :
           - 2 dimensional tensor.
 
## Norms
 Norms are used to quantify vector magnitude.
 
 * L2 Norm:
           - Measure simple(Euclidean) distance from origin.
           - ||X||2  = sqrt ( summation (sqr(xi))  for all i's
           
 * Unit Vector:  if ||x||2 = 1, then x is an unit vector.
 
 * L1 Norm :
           - || X ||1 = summation (abs(xi))
           - Varies linearly at all locations whether near or far from origin
           - Used whenever differnence between zero and non-zero is key.
           
 * Sqaured L2 :  || X || 2,2 = summation (sqr(xi)  for all i's
           - Computationally cheaper to use than L2 norm because:
               - Squared L2 norm equals simply X.t . X
               - Derivative (used to train naby ML algorithms) of element x requires that element alone, whereas L2 norm requires X vector.
           - Downside: it grows slowly near by origins so can't be used if distinguishing b/w zero and non-zero is important.
          
 * MaxNorm : ||X|| = max|xi|
 
 * Generalized Lp Norm:  
           ||X||p = pth root (sum( xi pow p)  p-> must be real number and >=1.
           
 * Norms are used to regularize objective functions.
 
## Basis Vectors:
 If you can write every vector in a given space as a linear combination of some vectors and these vectors are independent of each other then we call them as basis                                    vectors for that given space.
 - can be scaled to represent any vector in a given vector space.
 - typically unit vectors along axes of vector space.  for 2D  i(1,0) and j(0,1)
 - Must be liniearly independent of each other.
 - Must span the whole space.
 - Basis vectors are not unique.
 
 ## Orthogonal Vector
 X and Y are orthogonal if X.T * Y = 0
 
 ## Orthonormal : 
 Orthogonal and have unit norm. e.g Basis vector.
 
 ## Matrix Operations
 * Transpose of a matrix :
           - Xt(i,j) = X(j,i)
 * Hadamard Product - Element wise product. If two tensors have the sme size, operations are often by default applied element-wise. AoX
 
 * Reduction : Calculation of sum across all elements of a tensor.
           e.g for vector X of length n : sum(xi)
           e.g. fr matrix X with m by n : sum i (sum j x(i,j))
 
 * Dot Product (ubiquitous in DL) ; X.Y = Xt* y
 
 * Frobenius Norm : ||X||f = sqrt (sum(sqr(xij))
           - Analogous to L2 norm of vector
           - Measure size of matrix in term of Euclidean distance.
 
 * Symmetric Matices :
           - Should be square matrix
           - Xt = X : anything can be along the diagonal but symmetreic  otherwise
        
 * Identity Matrix :
           - Sqaure matrix with diagonal values 1 and other values as 0.
           - I3 = [[1,0,0],[0,1,0],[0,0,1]]
           - I.X = X
       
 * Matrix multiplication
           - m by n  multiplied by n by p then resultant will be m by p
           - Cik = sum( Aij . Bjk)
 
 * Inversion
           - Clever , convenient approach for solving linear equation
           - X(-1)X= I(n)
           - Xw = y ,
             X(-1)Xw = X(-1)y ,
             I(n)w = X(-1)y ,
             w = X(-1)y  : Thus unknown w is calculated using matrix inverse.
         
           - Matrix inversion can be calculated only if
              - Matrix isn't singular : i.e all columns of matrix must be linearly independent.
              - Matrix is square i.e n(row) = n(col) : vector space = matrix range
              - As it avoids
              1. Overdetermination : n(row) >n(col) i.e nof of equation > no of dimensions.
              2. Underdetermination : n(row) < n(col)
              
  * Diagonal Matrix : Non zero along diagonal and zero everywhere else. e.g Identity matrix.
           - Can be non-square and computation still efficient.
           - if h>w, simply add zeros to product
           - if w>h, remove elements from product
           
   
