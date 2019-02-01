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
- Basic knowledge of notebook-related tools like [Weave](https://github.com/mpastell/Weave.jl).

#### First steps

- Become familiar with the updated syntax of JuMP 0.19, its [documentation](http://www.juliaopt.org/JuMP.jl/dev/index.html) and [style guidelines](http://www.juliaopt.org/JuMP.jl/dev/style/)
- Become familiar with existing JuMP [example notebooks](https://github.com/JuliaOpt/juliaopt-notebooks)
- Become familiar with tools like [Weave](https://github.com/mpastell/Weave.jl)
- Make a small update to an existing notebook or develop a simple new notebook, and submit a pull request to [PolyJuMP](https://github.com/JuliaOpt/PolyJuMP.jl) on Github
- Explore JuMP extensions such as [PolyJuMP](https://github.com/JuliaOpt/PolyJuMP.jl)
