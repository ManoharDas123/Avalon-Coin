# Analysis of PRINT Cipher Sbox




# Sbox
It is a **3**-bit to **3**-bit single sbox used in PRINT Cipher
| x    | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|------|---|---|---|---|---|---|---|---|
| s[x] | 0 | 1 | 3 | 6 | 7 | 4 | 5 | 2 |


The Sbox has a linear structure.
It is a balanced sbox.


# DDT

The difference distribution is calculated using Sage

|       | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-------|---|---|---|---|---|---|---|---|
| **0** | 0  | 0 | 0 | 0 | 0 | 0| 0 | 0 |
| **1** | 0 | 2 | 0 | 2 | 0 | 2 | 0 | 2 |
| **2** | 0 | 0 | 2 | 2 | 0 | 0 | 2 | 2 |
| **3** | 0 | 2 | 2 | 0 | 0 | 2 | 2 | 0 |
| **4** | 0 | 0 | 0 | 0 | 2 | 2 | 2 | 2 |
| **5** | 0 | 2 | 0 | 2 | 2 | 0 | 2 | 0 |
| **6** | 0 | 0 | 2 | 2 | 2 | 2 | 0 | 0 |
| **7** | 0 | 2 | 2 | 0 | 2 | 0 | 0 | 2 |

The differential branch number of the sbox is 2.

## LAT
|       | 0  | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-------|---|---|---|---|---|---|---|---|
| **0** | 4  | 0 | 0 | 0 | 0 | 0| 0 | 0 |
| **1** | 0 | -2 | 0 | 2 | 0 | 2 | 0 | 2 |
| **2** | 0 | 0 | 2 | 2 | 0 | 0 | 2 | -2 |
| **3** | 0 | 2 | -2 | 0 | 0 | 2 | 2 | 0 |
| **4** | 0 | 0 | 0 | 0 | 2 | -2 | 2 | 2 |
| **5** | 0 | 2 | 0 | 2 | 2 | 0 | -2 | 0 |
| **6** | 0 | 0 | 2 | -2 | 2 | 2 | 0 | 0 |
| **7** | 0 | 2 | 2 | 0 | -2 | 0 | 0 | 2 |

The linear branch number of the sbox is 2. The linearity of this sbox is 4.

## Interpolation Polynomial

The interpolation polynomial is a univariate polynomial which is over an extension field representing the sbox.

The interpolation polynomial of this sbox is
**(a + 1)x^6 + (a^2 + a + 1)x^5 + (a^2 + 1)x^3**
## Polynomials
The polynomials which satisfy the given sbox is 
 

 - x0\*x2 + x0 + x1 + y1
 - x0\*x1 + x0 + x1 + x2 + y2 
 -  x0\*y1 + x0 + x2+ y1 + y2  
 - x0\*y2 + x1 + y1
 -   x1\*x2 + x0 + y0
 -  x1\*y0 + x1 + x2 + y0 + y2
 -   x0\*y0 + x1\*y1 + x2 + y2
 -   x1\*y2 + x0 + x1 + y0
 -   x2\*y0 + x1 + y0 + y1
 -   x2\*y1 + x0 + y0
 -   x0\*y0 + x2\*y2 + x0 + x1 + x2 + y0 + y1
 -   y0\*y1 + x2 + y0 + y1 + y2  
 - y0\*y2 + x1 + y1
 -  y1\*y2 + x0+ y0 + y1
 
 x - input variables
 y - output variables

## Other Properties

 - Max Degree of components functions -> **2**
 - Min Degree of components functions -> **2**
 - Maximal differential probability -> **0.25**
 - Absolute maximal linear bias -> **2**
 - Relative maximal linear bias -> **0.25**

