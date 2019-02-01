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
