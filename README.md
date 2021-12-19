# DVIP Fall 2021 - Exam Project

## ICIP 1 Submission

This repository implements Quarter Laplacian Filter for Edge Aware Image Processing using the approach mentioned in this
[paper](https://github.com/bonaventuredossou/dvip_project/blob/main/data/ICIP%201%20-%20QUARTER%20LAPLACIAN%20FILTER%20FOR%20EDGE%20AWARE%20IMAGE%20PROCESSING.pdf).

### Usage
Image smoothing is the fundamental operation in image processing. We use it to remove image details or noise in the
image. While performing smoothing operation, it is needed to remove small gradients and preserve the large ones which is
called edge preserving. This repository uses Laplasian filter originally obtained from diffusion equation.

### Implementation
It is implemented using classical box filter method but instead of using entire Laplacian Kernel this method uses
quarter of Laplacian Kernel.

Standard Laplacian Kernels are as follows:

<pre>
[0,   1/4, 0  ]   [-1/16, 5/16, -1/16]   [1/12, 1/6, 1/12]
[1/4, -1,  1/4] , [5/16,  -1,    5/16] , [1/6,  -1,   1/6]
[0,   1/4, 0  ]   [-1/16, 5/16, -1/16]   [1/12, 1/6, 1/12]
</pre>

This implementation uses right most Kernel which is the most isotropic kernel as mentioned in the paper. Therefore, the 
quarter Laplacian filters would be as follows:

<pre>
     [1/3, 1/3, 0]        [0, 1/3, 1/3]        [0,   0,   0]        [0,     0, 0]
K1 = [1/3, -1,  0] , K2 = [0,  -1, 1/3]   K3 = [0,  -1, 1/3] , K4 = [1/3,  -1, 0]
     [0,   0,   0]        [0,   0,   0]        [0, 1/3, 1/3]        [1/3, 1/3, 0]
</pre>

<!-- TO DO: After implementation -->

### Installation
Please just run install.sh as follows to complete installation: <br/>
$ ./install.sh

NOTE: Linux based OS or MacOS required to run this shell script.

### Authors
Bonaventure Dossou and Chirag Vaghela
