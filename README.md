# Blue Marble DGGS Raster Data Cube Example

<img width="100%" alt="image" src="https://github.com/user-attachments/assets/6a171796-e634-4f20-b1f0-d10ec0f01717" />

## Get Started

Access the data with [DGGS.jl](https://github.com/danlooo/DGGS.jl):

```julia
using DGGS
using Zarr
using GLMakie

p = open_dggs_pyramid(zopen("https://raw.githubusercontent.com/danlooo/blue-marble.dggs.zarr/refs/heads/master"))
plot(p, :Red, :Green, :Blue; scale_factor=1/25)
```


## Index

Coordinates or cell ids of DGGS zones were obtained using Snyder Eqal Area Projection followed by a linear transformation, yielding 5 matrices of the size n*2n where n is a power of 2:

<img width="1908" height="1367" alt="image" src="https://github.com/user-attachments/assets/bdf89408-3b7e-4674-aea9-b404a700db23" />
