# acornlib

Acorn's standard library of mathematical facts.

This repository is a mathematics library, written in Acorn, building up mathematics from the
inherent axioms. The implementation of the Acorn language itself, the integrated AI, and the VS Code extension
are handled in the [acorn repository](https://github.com/acornprover/acorn).
The code for the acornprover.org website,
including documentation, is in the [acornprover.org repository](https://github.com/acornprover/acornprover.org).

## Mathematical Concepts Implemented

### Natural Numbers (`nat.ac`)
- Peano arithmetic with inductive definition of natural numbers
- Complete arithmetic operations (addition, multiplication)
- Core properties: 
  - Addition and multiplication are commutative and associative
  - Multiplication distributes over addition
  - Properties of zero and successor function

### Integers (`int.ac`)
- Extended natural numbers with negative numbers
- Complete arithmetic, including negation
- Key properties including double negation and absolute value

### Rational Numbers (`rat.ac`)
- Implemented as fractions (pairs of integers)
- Complete field operations and properties
- Ordering and equivalence relations

### Real Numbers (`real.ac`)
- **Complete Construction**: Built using Dedekind cuts (proper definition of the reals)
- **Number Properties**:
  - Real line is densely ordered (between any two reals, there's another real)
  - Real line is complete (no "holes" - all convergent sequences have limits)
  - Rationals are dense in the reals (any real can be approximated by rationals)
  - Floor function exists (any real number can be rounded down to an integer)

- **Order Properties**:
  - Complete order relation (any two reals are comparable)
  - The ordering respects arithmetic (adding the same number preserves order)
  - Signs of numbers determine their position relative to zero
  - Transitivity holds (if a < b and b < c, then a < c)

- **Field Properties**:
  - Addition is commutative and associative
  - Additive identity (0) and inverse (-x) exist for all reals
  - Addition of positive numbers yields positive results
  - Cancellation laws hold for addition

- **Absolute Value**:
  - Absolute value is always non-negative
  - |x| = |-x| for all reals 
  - Triangle inequality properties

- **Min and Max**:
  - Minimum and maximum of two numbers always exist
  - Minimum of positive numbers is positive
  - Maximum and minimum preserve ordering

- **Approximation**:
  - Any real number can be approximated by rationals to arbitrary precision
  - Floor function: for any real x, there is a unique integer n with n ≤ x < n+1
  - Rationals can be found in any interval with non-empty intersection

- **Convergence and Limits**:
  - Cauchy sequences are properly defined
  - Every Cauchy sequence of reals converges to a real number
  - Limits interact with order (x_n → x and y_n → y with x_n < y_n implies x ≤ y)
  - Equivalence between Cauchy sequence definition and Dedekind cut definition

- **Metric Properties**:
  - Distance between real numbers is well-defined
  - Triangle inequality holds
  - Real line forms a complete metric space
  - Closeness relation is symmetric and transitive

### Complex Numbers (`complex.ac`)
- **Structure**: Implemented as ordered pairs of real numbers (a + bi form)
- **Operations**:
  - Addition and multiplication with correct formulas
  - Complex conjugation
  - Absolute value squared (|z|²)
  - Classification (real vs. imaginary)

- **Algebraic Properties**:
  - Complex numbers form a field (addition and multiplication are well-behaved)
  - Distributive, commutative, and associative laws hold
  - The complex numbers 0, 1, and i have their expected properties
  - Complex conjugation interacts properly with arithmetic operations

### Other Mathematical Structures

- **Pairs** (`pair.ac`): Basic pair structure for building compound types
- **Lists** (`list.ac`): Sequential collections with standard operations
- **Option** (`option.ac`): Type for representing optional values
- **Finite Sets** (`finite_set.ac`): Mathematical sets with standard operations
- **Multisets** (`multiset.ac`): Sets that allow repeated elements
- **Groups** (`group.ac`): Abstract algebraic structure with associative operation
- **Monoids** (`monoid.ac`): Groups with identity element
- **Metric Spaces** (`metric_space.ac`): Spaces with distance function

## How To Contribute

Please feel free to submit pull requests! The more we contribute, the smarter the AI gets.

To start, fork this repository by clicking the "fork" button on GitHub. Then, clone the fork to your machine.

To work on your fork, open the `acornlib` folder from VS Code. The extension ships with a copy of the Acorn library, but it will use your local fork instead when you are working on a file inside it.

When you're ready, push your code to your fork, and open a pull request in the main repository.

## What to Contribute

The current goal for `acornlib` is to support the mathematics needed for the most common theorem-proving benchmarks, like [miniF2F](https://github.com/facebookresearch/miniF2F/blob/main/lean/src/test.lean) and PutnamBench. We still need to implement several parts of high school and college level mathematics:

- Exponentiation
- The definition and properties of `e`
- ~~Complex numbers~~ (implemented)
- Trigonometry: sine, cosine, pi
- Vectors
- Matrices

If you're not sure where to start, jump into [Discord](https://discord.gg/RqXxaye4MC) and we're happy to discuss.