# OSQP

OSQP is a numerical optimization package for solving sparse convex quadratic programs. It is written in C, but also provides interfaces to the most popular languages for scientific computing. OSQP is based on the alternating direction method of multipliers (ADMM), which has the following advantages over other state-of-the-art methods:
- **Computational efficiency:** its iterations are computationally cheap
- **Fast convergence for moderate accuracy:** it typically requires few hundreds of iterations to find a good solution
- **Supports warm-starting:** providing a good initial guess reduces computation times considerably
- **Detects infeasible and unbounded problems:** provides certificates of primal and dual infeasibility without modifying the problem

## Mentors

- [Bartolomeo Stellato](https://github.com/bstellato)
- [Goran Banjac](https://github.com/gbanjac)
- [Paul Goulart](https://github.com/goulart-paul)
- [Ian McInerney](https://github.com/imciner2)


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





### User-provided linear algebra

| **Intensity**  | **Priority**  | **Involves**   | **Mentors**  |
| -------------  | ------------  | -------------  | -----------  |
| Moderate       | High          | Allow OSQP to use external and user-provided linear algebra implementations | [Goran Banjac](https://github.com/gbanjac), [Paul Goulart](https://github.com/goulart-paul), and [Bartolomeo Stellato](https://github.com/bstellato) |

#### Abstract

OSQP relies on a relatively small number of linear algebra routines. It uses a custom implementation of these routines, which makes the solver library-free, but its hard-coded linear algebra makes it impossible to run on non-standard hardware architectures such as GPUs. To be able to exploit specialized hardware architectures, one needs to abstract data structures and computationally intensive linear algebra routines, and link a specific implementation during code compilation.


#### Technical details

We will adopt an object-oriented approach to abstract data structures representing vectors and matrices, and define a set of operations on these structures, e.g., vector addition, matrix-vector multiplication etc. We will provide at least two implementations, but will also allow for user-definable implementations. Switching between various implementations will be made easy by setting appropriate flags during code compilation.

Such abstraction will not be used only to run OSQP on different hardware architectures, but also to optimize the solver for speed or memory. For instance, the current data structure representing a symmetric matrix stores only its upper-triangular part to reduce the memory footprint. However, evaluating the matrix-vector product would be parallelizable if the full matrix were stored. Hence, if memory is not an issue for a specific application, the user would prefer the latter implementation as it would be faster.

Moreover, we will be able to use existing BLAS libraries, which consist of linear algebra operations that are highly optimized for most common hardware architectures.

#### Helpful experience

- Basic knowledge of ADMM
- Prior work with CMake and BLAS libraries

#### First steps

- read the paper: https://arxiv.org/abs/1711.08013
- understand the numerical algorithm implemented by OSQP and the main computational bottlenecks



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
| Moderate       | Medium        | Implement code generation in C. Allow multiple code-generated solvers on a single system. | [Ian McInerney](https://github.com/imciner2), [Goran Banjac](https://github.com/gbanjac), [Bartolomeo Stellato](https://github.com/bstellato), and [Paul Goulart](https://github.com/goulart-paul) |

#### Abstract

#### Technical details

#### Helpful experience

#### First steps
