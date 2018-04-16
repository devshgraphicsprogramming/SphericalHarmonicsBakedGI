# SphericalHarmonicsBakedGI
A very old (circa 2010) irrlicht 1.7.1 experiment with baking SH probe grids for environment lighting

This does no pre-convolution or actual good BRDF function decomposition, the objects simply pick up the light from their surrounding and the initial lightmapping has nothing to do with the fake-GI.

There's no reflectance model, and hence no attenuation which would give absolutely zero convergence if the baking was applied iteratively.

The only thing this code does correct is probably cubemap to Spherical Harmonic conversion, and that is most probably still missing a final multiply or a divide by a factor of PI.


Code written by me at 15 so expect zero comments and bad C++ style.

The code has an extremely bad folder structure, only binary built libary of irrlicht 1.7.1 included (plus headers), hence may not exactly compile.

