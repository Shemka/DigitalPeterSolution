# Digital Peter Contest Solution
## Task description
Digital Peter is an educational task with a historical slant created on the basis of several AI technologies (Computer Vision, NLP, and knowledge graphs). The task was prepared jointly with the Saint Petersburg Institute of History (N.P.Lihachov mansion) of Russian Academy of Sciences, Federal Archival Agency of Russia and Russian State Archive of Ancient Acts.

Contestants are invited to create an algorithm for line-by-line recognition of manuscripts written by Peter the Great.

## Approach
All images were resized to 128x1024 and normalized. Also rotated images were in dataset, so I used simple heuristic for their rotation. Only Random rotations and crops were used as augmentaions. Only lines with the most frequent chars were chosen. Then I used NN with following architecture: custom resnet-like backbone for image feature extraction, 3 GRU-256 with 0.1 dropout and CTC loss. Then sequence of probabilites were encoded with greedy search.

## Public
![изображение](https://user-images.githubusercontent.com/27767885/111811872-90ea5a80-88e8-11eb-9938-7994c8c28ec6.png)
## Private
![изображение](https://user-images.githubusercontent.com/27767885/111812032-bb3c1800-88e8-11eb-8ec9-1eeae7f5b54b.png)
