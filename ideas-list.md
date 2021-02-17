# OSQP

OSQP is a numerical optimization package for solving convex quadratic programs. It is written in C, but also provides interfaces to the most popular languages for scientific computing. OSQP is based on the alternating direction method of multipliers (ADMM), which has the following advantages over other state-of-the-art methods:
- **Computational efficiency:** its iterations are computationally cheap
- **Fast convergence for moderate accuracy:** it typically requires few hundreds of iterations to find a good solution
- **Supports warm-starting:** providing a good initial guess reduces computation times considerably
- **Detects infeasible and unbounded problems:** provides certificates of primal and dual infeasibility without modifying the problem

## Mentors

- [Bartolomeo Stellato](https://github.com/bstellato)
- [Goran Banjac](https://github.com/gbanjac)
- [Paul Goulart](https://github.com/goulart-paul)
- Ian?


## Project Ideas

**GB:** *Maybe each of us can take a lead in one project. I will be adding stuff in the linear-algebra part now.*




### QP differentiation

| **Intensity**  | **Priority**  | **Involves**   | **Mentors**  |
| -------------  | ------------  | -------------  | -----------  |
| Moderate       | Medium        | Differentiate solutions of quadratic programs | [Bartolomeo Stellato](https://github.com/bstellato), [Goran Banjac](https://github.com/gbanjac), and [Paul Goulart](https://github.com/goulart-paul) |

#### Abstract

#### Technical details

#### Helpful experience

#### First steps





### User-definable linear algebra

| **Intensity**  | **Priority**  | **Involves**   | **Mentors**  |
| -------------  | ------------  | -------------  | -----------  |
| Moderate       | Medium        | Allow OSQP to use external and user-provided linear algebra libraries | [Goran Banjac](https://github.com/gbanjac), [Paul Goulart](https://github.com/goulart-paul), and [Bartolomeo Stellato](https://github.com/bstellato) |

#### Abstract

#### Technical details

#### Helpful experience

#### First steps





### Anderson acceleration

| **Intensity**  | **Priority**  | **Involves**   | **Mentors**  |
| -------------  | ------------  | -------------  | -----------  |
| Moderate       | Medium        | Implement the Anderson acceleration scheme to speed up convergence of ADMM | [Paul Goulart](https://github.com/goulart-paul), [Bartolomeo Stellato](https://github.com/bstellato), and [Goran Banjac](https://github.com/gbanjac) |


#### Abstract

#### Technical details

#### Helpful experience

#### First steps



### Support for embedded systems

| **Intensity**  | **Priority**  | **Involves**   | **Mentors**  |
| -------------  | ------------  | -------------  | -----------  |
| Moderate       | Medium        | Implement code generation in C. Allow multiple code-generated solvers on a single system. | Ian?, [Goran Banjac](https://github.com/gbanjac), [Bartolomeo Stellato](https://github.com/bstellato), and [Paul Goulart](https://github.com/goulart-paul) |

#### Abstract

#### Technical details

#### Helpful experience

#### First steps
