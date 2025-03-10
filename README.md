# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Solve by substitution:

T(n)= T(n/13) + 5

T(n/169) + 10
      
T(n/13^3 ) + 15
      
T(n/13^4) +20
      
...
      
T(n/13^i) + i*5

for i = log n

T(1) + logn*5 = 1 + logn*5 ∈ Θ(logn)


2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Solve by substitution:

T(n)= 13T(n/13) + 5

13(13T(n/13^2) + 5) + 5

13^2T(n/13^2) + 10

13^3T(n/13^3) + 15

...

13^iT(n/13^i) + i*5

for i = lg n

nT(1) + lgn*5 = n+lgn*5 ∈ Θ(n)


3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$


Solve by substitution:


T(n)= 13T(n/13) + 2n

13(13T(n/13^2) + 2n) + 2n
      
13^2T(n/13^2) + 28n

13^2(13T(n/13^3) + 2n) + 28n

13^3T(n/13^3) + 54n 

 ...
 
13^iT(n/13^i) + (2n * 13 * (i-1)) +2n  

for i = lg n

nT(1) + (2n * 13 * (log n -1)) +2n

n + 26n * log n - 24n  ∈ Θ(nlogn)
