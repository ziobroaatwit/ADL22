# ADL22

## 1. Introduction
-What is your MSE/MAE with linreg vs tuned network?
The MSE of my network reduced from 24.29 to 8.65, and my MAE was 1.90. I achieved this result by upping the first layer to 128 neurons, and adding 5 hidden layers in the middle each of which had 128 neurons. I then raised the epoch to 30, however it seems there was diminishing results past 26 or so. 
![image](https://user-images.githubusercontent.com/54987160/170630715-77067474-0972-48b4-bab2-5994e9969b9e.png)

When adding the 5 layers of 128 neurons alone without changing the Epoch, the MSE is more mediocre, scoring only 13.17 for the MSE, meaning there was much more room to improve. 

## 2. Intro to convolution operations: Padding.
-What is a response layer? (Give a brief, 1-sentence description)
A response layer is the result of a convolution using a filter, when multiple layers are used they become stacked. 
-Given the filter shape of (26, 26, 32), what does each number represent?
26x26 resolution/shape of grid. 32 filters.
-Given 6x6 input and filter of (3,3): what is the response shape that we get? 
If I followed the lecture correctly, it will be 5x5, resulting in 25 responses. 
-Given (33, 33, 1) input and filter of (2,2): what is the response shape that we get? 
33-2+1, so (32,32)
-What is the difference between ‘valid’ and ‘same’ padding? Given 6x6 input and filter of (3,3),
Valid = no padding, so 6-3+1 you'd get a shape of 4x4. With Same padding, padding will be added such that output=input responses. Thus the shape will be (6,6). 
-what are the response shapes for both options? 
(4,4) for Valid, (6,6) for Same. 
