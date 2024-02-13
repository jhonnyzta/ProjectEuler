# Project Euler 3: Multiples of 3 or 5
#### <p align="right">by: Effe Zapata</p>

### Statement

If we list all natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Find the sum of all multiples of 3 or 5 below 1000.

### Solution

If we need to add all the numbers that are multiples of an integer x less than M, then we have the following:

$$ x+2x+3x+4x+.... m \cdot x$$

where $m= \lfloor \frac{M}{x} \rfloor$, then we have:

$$ x \cdot (1+2+3+ \cdots+m) = x\cdot \sum_{i=1}^{m} {i} = x \left(\frac{m(m+1)}{2}\right)$$

But we need to add all the numbers that are multiples of two integers x,y less than M, we cannot add directly $x\cdot\sum {j}$ and $y \cdot \sum {j}$ because there can be numbers that are both multiples of $x$ and $y$, that is, the multiples of $z=gcd(x,y)$ are being added twice. So it is necessary to subtract the multiples of z less than M. Let S be the sum of the multiples of $x$ and $y$ that are less than M, then:

$$ S = x \cdot \sum_{i=1}^{m}{i}+y \cdot \sum_{j=1}^{n}{j}-gcd(x,y)\sum_{k=i}^{r}{k}$$

Where we have $m= \lfloor \frac{M}{x} \rfloor$, $n= \lfloor \frac{M}{y} \rfloor$ and $r= \lfloor \frac{M}{gcd(x,y)} \rfloor$, therefore:

$$\begin{equation} S= x \cdot \frac{n(n+1)}{2}+y\frac{m(m+1)}{2}-gcd(x,y)\frac{r(r+1)}{2} \end{equation}$$


> ⚠️ **Remeber** x,y &#x2208; &#x2124; and the expresion &#x23A3; &#x2022; &#x23A6; it's the floor function.

### Code

|| Language  |      Time      |  Note | |
|:-:|----------|:-------------:|:------:|--|
|![julia](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/64449037-acae-4f72-a49a-d4b587b1b638)| Julia |   **747**   |  🥳 | |
|![cpp](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/168fd9cb-5554-441b-9d17-71642b3ac956)| C++ |1042 | 🤨 | |
|![rust](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/38212ef8-b357-4ded-b852-dd5530a2b3d3)| Rust | 2088 |😎 | |
|![python](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/ba32a2c1-8535-4d50-85ac-8e7e96a3a6aa)| Python |  18121 | 😱 | |
|![java](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/a6f44277-4820-4a11-b6d4-8567f129b2b0)| Java | 24052 | 🥶 | |


| | Languaje| Time| Note | optimization |
|:-:|----------|:-------------:|:------:|--|
|![javac](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/ea322cef-dde0-4acc-9747-e5ff1e8e0426)| Java+C |2522 | 🥹| 89.51%|
|![pythonc](https://github.com/jhonnyzta/ProjectEuler/assets/70600594/15fdc43d-d714-4392-86f1-6cb66caacd0d)| Python+C | 4898 | 🥹| 72.97%|

