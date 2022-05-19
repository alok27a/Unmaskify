# Unmaskify 😷
 Unmasking face mask from human faces. There are many places where we need to remove masks for authentication purpose like in Airport. Whenever we enter the airport, security asks for AADHAR card for verification purpose then we need to remove our mask. So, instead of removing your masks we can inpaint and reconstruct  
	 
 ![image](https://user-images.githubusercontent.com/73957024/169319599-b10e102b-1420-4cf7-891f-070c4d4133bf.png)
## Approach to solve this problem 📃
In this study, we employed the DCGAN model, however our framework is orthogonal to any GAN model that may be chosen. G, the generative model, is organised as follows: The input is a 100-dimensional random noise vector taken from a uniform distribution between [-1, 1], followed by an 8192 completely connected layer reconfigured to 4x4x512 dimensions. Each of the next levels is a deconvolutional layer, in which the number of channels is halved and the picture dimension is doubled compared to the preceding layers. The output layer has a dimension of 64x64x3, which is the size of the picture space. 
![image](https://user-images.githubusercontent.com/73957024/169319913-d85d0f91-0acf-4303-a5a6-d977c941a617.png)

The discriminating model, D, on the other hand, is built essentially backwards. The input layer is a 64x64x3 picture, followed by a succession of convolution layers that halve the image dimension and double the number of channels from the previous layer, and the output layer is a two class softmax. 

![image](https://user-images.githubusercontent.com/73957024/169319991-89ab18ae-38ad-42e4-9627-29e22ddf5210.png)
