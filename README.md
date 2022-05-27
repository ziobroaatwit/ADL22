# ADL22

##1. Introduction
-What is your MSE/MAE with linreg vs tuned network?
The MSE of my network reduced from 24.29 to 8.65, and my MAE was 1.90. I achieved this result by upping the first layer to 128 neurons, and adding 5 hidden layers in the middle each of which had 128 neurons. I then raised the epoch to 30, however it seems there was diminishing results past 26 or so. 
![image](https://user-images.githubusercontent.com/54987160/170630715-77067474-0972-48b4-bab2-5994e9969b9e.png)

When adding the 5 layers of 128 neurons alone without changing the Epoch, the MSE is more mediocre, scoring only 13.17 for the MSE, meaning there was much more room to improve. 
