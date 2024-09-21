# komorebi
sunlight filtering through trees


![result](generated/movie.webp "result")


While it is true that further down in the tree the sun has not changed in apparent size, 
but the leaves further up are now relatively smaller, this is not how the projection works.

The projection of the sun by a pinhole further up is proportionally larger.
Therefore it is enough to convolve the higher layers of leaves with a larger "sun" and the lower ones with a smaller one.

Multiplying the layers works to simulate the projection operation, so that direct light form one layer gets properly blocked by another while preserving the interacion of halos.
I am not sure whether this is fully accurat, but it looks good to my eyes.

Finally I apply a gamma curve to simulate diffuse lighting and eye response.

The layers are wiggled around to simulate wind.
I use pytorch to accelerate the convolution operation.

final code is in komorebi_nicer.ipynb