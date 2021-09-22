# Author
Jiajin Chen

# Image Classification using NMF 

The project details the use of Non-negative Matrix Factorization to factorize 2 datasets: ORL dataset and Extended YaleB dataset. Initially the data is clean, thus we manually add noise to the datasets by adding salt and pepper block points and Gaussian noises. To factorize matrices including noises, 2 algorithms of NMF has been chosen: simple NMF and L1-RNMF.

## Description
The first simple NMF method is to factorize the matrix to 2 simpler sub-matrices in addition to the equation of: V = W*H where W, H are the decomposition result of V with less dimensions.
The second method we chose is L1-RNMF, a method based on robust Non-negative Matrix Factorization via L1 Norm. 

### Noise-Choice &Pre-processing:
Based on the 2 datasets we chose, all the data we imported are the “clean data” without any noise, to examine the algorithms against noise impacts, the noises would be added noises to the dataset and the subsets would be produced correspondingly. Due to the high complexity of the original dataset, we decided to resize the YaleB image datasets from 192 x 168 to 48 x 42 by dividing the image size by 4 for both height and weight, and resize the ORL databases images from 112 * 92 to 56 * 46 by a reduce size of 2 for both height and weight.

The first method we used was to add salt and pepper noises. As a result, part of the picture would be blocked by a white noise points and this create noise for our data. We chose a number of 0.1, representing that 10% of the pixel values in an image was modified to white noise points. We chose a r number of 0.5, meaning that 50% of the modified pixel value should be 255(white). 

The second method we used to add noise is Gaussian noise. This is a noise type that follows a probability distribution of normal distribution
With a higher variance, the distribution of the noise would be more separated across the whole picture. And we wish to have a relatively evenly distributed noise, so a variance of 10 is chosen with a mean of 0. G-ratio stands for the level of blurry of the picture, here we wish to create some level of noise but also not too much as it might cause significant accuracy problems when we implement the decomposition. Hence, a g-ratio of 2 is chosen.

### Spacial set up
To collect the data, i put my phone and laptop 2 meters apart from each other in the same room, and there was no obstacle in between so LoS was satisfied, and both of them were placed on 2 chairs with the same height. 

### Data Collection
Data set is given in the data.zip file


## Getting Started

### Programming language
* Python 3
* Version: 3

