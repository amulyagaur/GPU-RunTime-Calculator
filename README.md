# GPU-RunTime-Calculator
Calculating-Time Prediction of GPU

It's very common to use GPUs to perform parallel computation in today's computationally demanding tasks, especially modern tasks like deep learning and high end graphic video games.

The experiment was run on a system running Ubuntu 16.04 Linux with an Intel Core i5 (3.5GHz), 16GB RAM, and a NVidia Geforce GTX 680 4GB GF580 GTX-1.5GB GPU. You need to predict the time this GPU takes (in the above mentioned system configuration) to multiply 2 matrices of size 2048x2048.

# Evaluation metric
RMSE 

# File Description
train.csv - training data<br>
test.csv - testing data<br>
sampleSubmission.csv - a sample file similar to what you need to upload

# Data field Description
Independent variables:

col 1-2. MWG, NWG: per-matrix 2D tiling at workgroup level: {16, 32, 64, 128} (integer)

col 3. KWG: inner dimension of 2D tiling at workgroup level: {16, 32} (integer)

col 4-5. MDIMC, NDIMC: local workgroup size: {8, 16, 32} (integer)

col 6-7. MDIMA, NDIMB: local memory shape: {8, 16, 32} (integer)

col 8. KWI: kernel loop unrolling factor: {2, 8} (integer)

col 9-10. VWM, VWN: per-matrix vector widths for loading and storing: {1, 2, 4, 8} (integer)

col 11-12. STRM, STRN: enable stride for accessing off-chip memory within a single thread: {0, 1} (categorical)

col 13-14. SA, SB: per-matrix manual caching of the 2D workgroup tile: {0, 1} (categorical)

Target Variables: 15-18. Run1, Run2, Run3, Run4: performance times in milliseconds for 4 independent runs using the same parameters. They range between 13.25 and 3397.08.

# [Contest Link](https://www.kaggle.com/c/logicalrhythm18-gpu/)

# Result 
Rank : 1
Score : 1.65440
