# Radar object detection

## 2D CFAR Implementation

1. Two for loops are used to loop over each element in the RDM array, thereby during each iteration one cell is considered Cell Under Test (CUT) from the grid.
2. The average noise value is then calculated
3. The threshold is converted using pow2db and the offset value is added to the threshold
4. If the CUT is greater than the threshold, it is replaced by 1 otherwise 0

## Selection of Training, Guard cells and offset

* Range Training cells = 10, Doppler Training cells = 8.
* Range Guard cells = 4, Doppler Guard cells = 4.
* offset = 1.2 

## Suppress the non-thresholded cells at the edges
The output RDM is cutout so that the surrounding rows and columns depend only on the range and doppler training cells.
