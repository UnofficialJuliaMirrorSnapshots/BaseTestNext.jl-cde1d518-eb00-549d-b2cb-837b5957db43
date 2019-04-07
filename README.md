# BaseTestNext

[![Build Status](https://travis-ci.org/JuliaCI/BaseTestNext.jl.svg?branch=master)](https://travis-ci.org/JuliaCI/BaseTestNext.jl)
[![codecov.io](http://codecov.io/github/JuliaCI/BaseTestNext.jl/coverage.svg?branch=master)](http://codecov.io/github/JuliaCI/BaseTestNext.jl?branch=master)

[![BaseTestNext](http://pkg.julialang.org/badges/BaseTestNext_0.4.svg)](http://pkg.julialang.org/?pkg=BaseTestNext)
[![BaseTestNext](http://pkg.julialang.org/badges/BaseTestNext_0.5.svg)](http://pkg.julialang.org/?pkg=BaseTestNext)

The `Base.Test` module changed substantially internally in
Julia `v0.5`. Most use cases are unaffected, but some features
such as `Test.with_handler` were removed, and many new features
were added. This package provides the new `Base.Test` functionality
so that packages that are supporting Julia `v0.4` can use them.

For documentation, please refer to the
[Julia manual](http://docs.julialang.org/en/latest/stdlib/test/).


### Usage

Replace `using Base.Test` with:

```julia
if VERSION >= v"0.5.0-dev+7720"
    using Base.Test
else
    using BaseTestNext
    const Test = BaseTestNext
end
```

See also
[BaseTestDeprecated.jl](https://github.com/JuliaCI/BaseTestDeprecated.jl),
which provides the Julia `v0.4`-and-earlier `Base.Test` for packages that
support Julia `v0.5` and use one of the removed features.
