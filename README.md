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
