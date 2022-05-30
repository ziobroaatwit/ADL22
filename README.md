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

## 2. Convolution Parameters: Stride and Pooling
- What is max pooling? (Give a brief, 1-sentence description)
Max pooling is using our filters like before, and checking for the largest value of that location, and making that the downsample. EG: A block of 1,3,4,5 becomes a block of 5. 

- If I apply pooling of 2 (2,2 window with a stride of 2) to a (6,6) array, what is the resulting size? 
(3,3)


## 4. ConvNet Architectures, layers
-Define I, O, F, S, P as used in this lecture (Give a brief, 1-sentence description)
I is the input resolution eg 7x7.
O is the expected output size.
F is the filter or kernel size. Default = 3x3. 
S is the stride size of the operation.
P is the amount of padding used.

-What is my output size if Input = (100, 100), kernel size=(2, 2), the stride of 1, and no pooling? 
(99,99)

-How many weights do I have if I have 24 such filters stacked (conv2_24)?
Well you didn't give me an input to work with, but let's assume it's 100,100? I did (2,2)x24=96, assuming the same logic as 224x224x3 being (3,3,3)x64=1728. Correct me if I'm wrong here.

-Solve for the padding (P), in terms of I, F, and S, if we want the input and output size to remain the same. 
P=(OxS-S-I+F)/2 Assuming O==I and is !=0.

## 5. Practical patterns
-What can we use the ImageDataGenerator for? What can it help us fight? (Give a brief, 1-sentence description)
The video is bugged, so it's impossible to watch. I asked a classmate to check and it just skips to the end without letting us watch it. So, I can't answer these. 🤷‍♂️
-What is a better idea: To use one larger kernel (8,8) or multiple stacked smaller ones, 4x(2,2)? Why? Show the number of weights for each option. 
