# JuMP

JuMP is a modeling interface and a collection of supporting packages for mathematical optimization that is embedded in Julia. With JuMP, users formulate various classes of optimization problems with easy-to-read code, and then solve these problems using state-of-the-art open-source and commercial solvers. JuMP also makes advanced optimization techniques easily accessible from a high-level language.

## Mentors

- [Chris Coey](https://github.com/chriscoey)
- [Carleton Coffrin](https://github.com/ccoffrin)
- [Joaquim Dias Garcia](https://github.com/joaquimg)
- [Oscar Dowson](https://github.com/odow)
- [Lea Kapelevich](https://github.com/lkapelevich)
- [Benoît Legat](https://github.com/blegat)
- [Miles Lubin](https://github.com/mlubin)
- [Sascha Timme](https://github.com/saschatimme)
- [Juan Pablo Vielma](https://github.com/juan-pablo-vielma)


## Project Ideas

###  Solver Tests and Benchmarks

#### Abstract

MathOptInterface is a very general way of representing a mathematical optimization problem. This project will develop infrastructure to test the correctness of, and benchmark, MathOptInterface-compatible solvers in Julia.


| **Intensity**                          | **Priority**              | **Involves**  | **Mentors**              |
| -------------                          | ------------              | ------------- | -----------              |
| Moderate  |  Medium  | Converting existing benchmark libraries into MathOptFormat. Developing infrastructure to make testing and benchmarking MathOptInterface-compatible solvers easy.         | [Chris Coey](https://github.com/chriscoey), [Carleton Coffrin](https://github.com/ccoffrin) and [Oscar Dowson](https://github.com/odow) |

#### Technical Details

The generality of [MathOptInterface’s standard form](http://www.juliaopt.org/MathOptInterface.jl/dev/apimanual/) enables it to model problems that cannot be written down in existing file-formats for optimization models (e.g., a mixed-integer problem with both NLP and conic constraints). To overcome this problem, a new file format is under development, [MathOptFormat](https://github.com/odow/MathOptFormat.jl). By converting existing benchmark libraries of optimization models into MathOptFormat, we can have a centralized and diverse library of models for testing and benchmarking Julia solvers that are hooked into MathOptInterface.
The main goals of this project are to:
- Automate the conversion of existing benchmark libraries such as [CBLib](http://cblib.zib.de/) and [MINLPLib](http://www.minlplib.org/) into MathOptFormat
- Make this library accessible online
- Develop Julia infrastructure to make downloading, reading, and running these MathOptFormat instances easy for the purpose of testing and benchmarking optimization solvers in Julia
- Extend/improve [MathOptFormat](https://github.com/odow/MathOptFormat.jl) as necessary


#### Helpful Experience

- Basic knowledge of JuMP v0.19
- Prior work with optimization solvers
- Experience with testing or benchmarking numerical code


#### First steps

- Become familiar with [MathOptFormat](https://github.com/odow/MathOptFormat.jl) and various standard file formats for optimization models such as .MPS, .CBF, .NL, and .LP
- Become familiar with testing and benchmarking tools in Julia
- Become familiar with current testing and benchmarking infrastructure in [JuMP](https://github.com/JuliaOpt/JuMP.jl) and [MathOptInterface](https://github.com/JuliaOpt/MathOptInterface.jl), solvers such as [Pajarito](https://github.com/JuliaOpt/Pajarito.jl), and [MINLPLibJuMP](https://github.com/lanl-ansi/MINLPLibJuMP.jl) and [PowerModels](https://github.com/lanl-ansi/PowerModels.jl)

###  New and Updated Example Notebooks

#### Abstract

With the upcoming v0.19 update to JuMP many example notebooks need to be updated. This is also a great opportunity to add new examples and improve their accessibility.

| **Intensity**                          | **Priority**              | **Involves**  | **Mentors**              |
| -------------                          | ------------              | ------------- | -----------              |
| Easy |  Medium  | Porting notebook examples to JuMP v0.19, improving and standardizing notation, naming, and style, developing new notebooks, linking to JuMP documentation, etc.        | [Chris Coey](https://github.com/chriscoey), [Joaquim Dias Garcia](https://github.com/joaquimg) and [Lea Kapelevich](https://github.com/lkapelevich)|

#### Technical Details

The soon to be released version 0.19 of [JuMP](https://github.com/JuliaOpt/JuMP.jl) introduces many syntax changes that will require updates to many [example notebooks](https://github.com/JuliaOpt/juliaopt-notebooks). Many JuMP extensions such as [PolyJuMP](https://github.com/JuliaOpt/PolyJuMP.jl) could also benefit from new example notebooks. This is also a good opportunity to improve these examples in various ways such as:
- Standardizing naming and structuring of examples to enforce [JuMP style guidelines](http://www.juliaopt.org/JuMP.jl/dev/style/)
- Linking to parts of specific examples from the [JuMP documentation](http://www.juliaopt.org/JuMP.jl/dev/index.html), and try to cover all important JuMP functionality with examples
- Adding examples for all [major solvers](http://www.juliaopt.org/#solvers) and linking to the examples from solver readmes
- Making it easy for people to try out JuMP examples with open-source solvers in the browser without downloading Julia
- Using tools like [Weave](https://github.com/mpastell/Weave.jl) to facilitate the development and deployment of the examples


#### Helpful Experience

- Basic knowledge of JuMP v0.19
- Basic knowledge of mathematical optimization models and methods
- Basic knowledge of notebook-related tools like [Weave](https://github.com/mpastell/Weave.jl)

#### First steps

- Become familiar with the updated syntax of JuMP 0.19, its [documentation](http://www.juliaopt.org/JuMP.jl/dev/index.html) and [style guidelines](http://www.juliaopt.org/JuMP.jl/dev/style/)
- Become familiar with existing JuMP [example notebooks](https://github.com/JuliaOpt/juliaopt-notebooks)
- Become familiar with tools like [Weave](https://github.com/mpastell/Weave.jl)
- Make a small update to an existing notebook or develop a simple new notebook, and submit a pull request to [PolyJuMP](https://github.com/JuliaOpt/PolyJuMP.jl) on Github
- Explore JuMP extensions such as [PolyJuMP](https://github.com/JuliaOpt/PolyJuMP.jl)


### Experiments with Automatic Differentiation (AD) Backends for JuMP

#### Abstract

JuMP's Automatic Differentiation (AD) library for computing derivatives of
nonlinear models was written before the recent emergence of advanced AD
libraries in Julia. JuMP's AD imposes a number of
[syntax limitations](http://www.juliaopt.org/JuMP.jl/0.18/nlp.html#syntax-notes)
that are difficult to address within the current framework. Performance could
also be improved. Hence, we would like to explore whether other libraries have
the potential to integrate with JuMP as replacement AD backends.

Mentors: [Miles Lubin](https://github.com/mlubin) and
[Juan Pablo Vielma](https://github.com/juan-pablo-vielma)

#### Technical Details

The goal of this project is to evaluate if existing AD libraries in Julia can
serve as replacements for JuMP's AD. This involves implementing benchmarks for
gradient and Hessian computations in multiple backends and comparing performance
and functionality.

Stretch goals:
- A prototype translation layer between JuMP and a new AD backend, or
- A frontend to [MOI](https://github.com/JuliaOpt/MathOptInterface.jl) nonlinear
  solvers using a different AD backend.


#### Helpful Experience

- Familiarity with JuMP’s non-linear optimization interface
- Familiarity with some of Julia’s Automatic Differentiation libraries
  including:
  
  - [Flux](https://github.com/FluxML) / [Tracker](https://github.com/FluxML/Tracker.jl)
  - [Zygote](https://github.com/FluxML/Zygote.jl)
  - [ForwardDiff](https://github.com/JuliaDiff/ForwardDiff.jl)
  - [Nabla](https://github.com/invenia/Nabla.jl)
  - [ReverseDiff](https://github.com/JuliaDiff/ReverseDiff.jl)

  
 Its is also useful to know about:
  - [Cassette](https://github.com/jrevels/Cassette.jl)
  - [ChainRules](https://github.com/JuliaDiff/ChainRules.jl)
  
#### First steps

- Watch Miles's [JuliaCon talk](https://youtu.be/xtfNug-htcs) on JuMP's AD
- Read Section 5 of the [JuMP paper](https://mlubin.github.io/pdf/jump-sirev.pdf)
- Update `acpower` and `clnlbeam`
  [benchmarks](https://github.com/mlubin/JuMPSupplement) for JuMP 0.19.
- Implement these two benchmarks in another Julia AD library for comparison of
  performance.

###  MutableArithmetics

#### Abstract

Create a MutableArithmetics (MA) package in which mutable versions of the arithmetic operations are defined. This package allows 1) for mutable types to implement a mutable arithmetics 2) for algorithms that could exploit mutable arithmetics to exploit it while still being completely generic.

| **Intensity** | **Priority** | **Involves**  | **Mentors**              |
| ------------- | ------------ | ------------- | -----------              |
| Hard          |  Medium      | Creating/documenting/testing a new API. Benchmarking code. | [Benoît Legat](https://github.com/blegat) and [Sascha Timme](https://github.com/saschatimme) |

#### Technical Details

Julia define standard arithmetic functions such as `+`, `-`, `*`, `/`, …
which allows generic code to be usable by any type implementing the appropriate methods.
For instance, `sum(::Vector{T})` works as long as `+(::T, ::T)` is defined.
However, this generic implementation relying on `+` may not be optimal if `T` is a mutable type.
For instance, if `T` is `JuMP.VariableRef`, and the vector has length `n`,
the generic `sum` will allocate intermediate affine expressions of length 2, 3, 4, …, `n`
resulting in `O(n^2)` complexity.
For this reason, a [specialized method is defined in JuMP for summing affine expressions](https://github.com/JuliaOpt/JuMP.jl/blob/f46a461c126fd1a7c309fb773a00b5dc529632b9/src/operators.jl#L304-L310)
that creates an empty affine expression and mutates its by adding each expression in the sum using `JuMP.add_to_expression!`.
This method has `O(n)` complexity for summing `n` variables.
The need for such specified methods is not specific for JuMP and is in general required for any mutable type,
see for instance the [`sum` method for `BigInt`](https://github.com/JuliaLang/julia/blob/d4018df968019d38943cd5009fe469f1e97ba0b6/base/gmp.jl#L549) which uses `MPZ.add!` to accumulate the sum in the same `BigInt`.
Because there is no standardized function for summing two object and allowing to mutate the first one,
mutable types have to create specific methods (such as `JuMP.add_to_expression!` or `MPZ.add!`) and reimplement a specific method for each function that can take advantage of its mutability (such as `sum`).
In JuMP, the mutating ability of its affine and quadratic expressions are exploited in two ways:

- First, specialized methods for standard Base functions are implemented in `src/operators.jl` such as `sum`, matrix products, …
- Second, when written inside a JuMP macro such as `@constraint`, an expression such as `3x + 2y + z - u + w` is rewritten to use a mutating function `JuMP.destructive_add!` (see `src/parse_expr.jl`).

While this covers most use cases,
it does not allow generic algorithms to take advantage of the mutability of JuMP expressions as it needs to use either `JuMP.add_to_expression!` or `JuMP.destructive_add!`.
For instance, when the coefficients of polynomials are JuMP expressions,
the generic operations defined in the https://github.com/JuliaAlgebra/ packages are suboptimal.
Moreover, the rewritting rules used in the JuMP macro does not exploit the mutability of mutable types such as polynomials.
Therefore in `3x + 2y + z - u + w`, if `x`, `y`, `z`, `u` and `w` are polynomials,
as they do not implement `JuMP.add_to_expression!` or `JuMP.destructive_add!`,
the rewritting with fallback to using the non-mutating `+`.
In this project, a MutableArithmetics (MA) package is created in which mutable versions of the arithmetic operations are defined.
This package allows

1. for mutable types to implement a mutable arithmetics
2. for algorithms that could exploit mutable arithmetics to exploit it while still being completely generic.

The student will be asked to complete some of the following tasks after creating the MA package

- Implement the MA API in MOIU and JuMP
- Use the MA API in JuMP.parseExpr instead of JuMP.destructive_add
- Implement the MA API for mutable types in Base such as BigInt in MA (so that MA could tests itself).
- Use MA in MultivariatePolynomials/DynamicPolynomials/TypedPolynomials: This would allow polynomial operation to be more efficient when the element type is BigInt, MOI functions or JuMP functions.
- Implement MA for MultivariatePolynomials/DynamicPolynomials/TypedPolynomials: This would allow polynomial arithmetics to be done efficiently in JuMP macros.
- Move JuMP.parseExpr and related code to MA, it should be able to define an “@expression(expr)” macro that replace “expr” with an equivalent expression which use MA instead of allocating many intermediate results. Example: @expression(a + b + c) would be rewritten as “res = copy(a); operate!(+, res, b); operate!(+, res, c)”.
  This would allow types that implement the MA API to benefit from this feature.

#### Helpful Experience

- Notions of computational complexity. Basic knowledge on Benchmarking
- Familiarity with JuMP representation of affine and quadratic expressions
- Familiarity with https://github.com/JuliaAlgebra/MultivariatePolynomials.jl

#### First steps

- Write simple benchmarks with https://github.com/JuliaAlgebra/MultivariatePolynomials.jl and JuMP/MOI which would benefit from MA
- Read performance tips https://docs.julialang.org/en/v1/manual/performance-tips/index.html

###  Automatic Dualization

#### Abstract

Sometimes solving the dual of an optimization problem is faster than solving the original problem. The goal of this project is to create a tool similar to the [automatic dualization features in YALMIP](https://yalmip.github.io/tutorial/automaticdualization/).

| **Intensity** | **Priority** | **Involves**  | **Mentors**              |
| ------------- | ------------ | ------------- | -----------              |
| Moderate      |  Medium      | Writing [MOI](https://github.com/JuliaOpt/MathOptInterface.jl) code. Using duality theory in optimization. | [Chris Coey](https://github.com/chriscoey) [Joaquim Dias Garcia](https://github.com/joaquimg) [Benoît Legat](https://github.com/blegat) |

#### Technical Details

Duality [plays a central role in optimization in optimization](http://web.stanford.edu/~boyd/cvxbook/).
For many solvers, the primal and dual form are different and it sometimes
renders the problem easier to solve if it is converted into the dual form
see the [automatic dualization features in YALMIP](https://yalmip.github.io/tutorial/automaticdualization/).

Moreover, there are applications that require solving the KKT conditions for an optimization problem.
This is the case of multilevel optimization, in which some constraints of an optimization problem include another optimization problem.
Many classes of problems in [Extended Mathematical Programming](https://www.gams.com/latest/docs/UG_EMP.html) (EMP) such as MPECs,
EPECs and so on, can be easily modeled if the KKT conditions can be automatically obtained from the primal problem.
(https://www.gams.com/latest/docs/UG_EMP.html, https://github.com/xhub/EMP.jl)

#### Helpful Experience

- Basic knowledge of JuMP v0.19 and MOI
- Understanding of basic duality theory for linear and conic optimization
- Basic knowledge of mathematical optimization models and methods

#### First steps

- Become familiar with [MathOptInterface’s standard form](http://www.juliaopt.org/MathOptInterface.jl/dev/apimanual/)
