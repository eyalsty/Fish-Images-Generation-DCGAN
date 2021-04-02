### Fish-Images-Generation-DCGAN

implementation of a DCGAN (Deep Convolutional Generative Adversarial Network) model that would learn how to generate fake pictures of fish types from a large dataset of fish images found on Kaggle.

Moreover, there is a implementation of a vanilla GAN as well, comparing the networks with the intention of showing that DCGAN is the superior network.

## Vanilla GAN

# Loss graph
 
 ![image](https://user-images.githubusercontent.com/45969711/113431146-f9a2fe00-93e3-11eb-858f-5401900fd884.png)


As we can see in the graph, the results are looking as expected: The loss of both the discriminator and the generator is fluctuating, as it should, and there is no increase over time since the graphs always goes up and down in the same range for both networks.


#Model progression over time
![image](https://user-images.githubusercontent.com/45969711/113431241-1d664400-93e4-11eb-9578-940f8ecefcb0.png)

We can see that the model starts with a random noise, a
pixelated image, and slowly the image is starting to
resemble a fish more and more as the training proceeds
and the number of epochs increases. However, even after
50 epochs, the image is still very blurry, unclear and in a
bad quality.
We would like to see how the DCGAN differs, as we expect
the DCGAN model to yield better results than what we see
here.

## DCGAN
# Loss graph

![image](https://user-images.githubusercontent.com/45969711/113431285-2fe07d80-93e4-11eb-9316-87a7b036a190.png)

(Notice: this time the blue graph is the Generator, as opposed to the first graph)
In this graph, the results are looking as expected as well, since the loss of both networks is fluctuating, but now we can see that there is a major decrease in the generator loss before it starts to fluctuate. This implies that there is a much faster learning process in the DCGAN model than the vanilla GAN model.

# Model progression over time!

0:
![image](https://user-images.githubusercontent.com/45969711/113431412-674f2a00-93e4-11eb-90fc-f0b0199da452.png)

10:
![image](https://user-images.githubusercontent.com/45969711/113431425-6c13de00-93e4-11eb-8228-549bf91268f7.png)

20:
![image](https://user-images.githubusercontent.com/45969711/113431453-71712880-93e4-11eb-814a-f8e261c93aa3.png)

30:
![image](https://user-images.githubusercontent.com/45969711/113431461-746c1900-93e4-11eb-8f3c-82c0da2c7b43.png)

50:
![image](https://user-images.githubusercontent.com/45969711/113431474-77ffa000-93e4-11eb-940d-c342d6699dc6.png)

As we can see in the results above, 10 epochs of the DCGAN training are more than enough to produce much better images than the images the vanilla GAN generates after 50 epochs.
The output after 50 epochs looks incredibly real, meaning the model works well.

Helped by:
* https://www.youtube.com/watch?v=OljTVUVzPpM&ab_channel=AladdinPersson![image](https://user-images.githubusercontent.com/45969711/113431716-d62c8300-93e4-11eb-803f-19ad1221f082.png)
* Explanation and implementation of DCGAN by PyTorch: https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html

Difference between GAN and DCGAN:
* https://datascience.stackexchange.com/questions/32671/gan-vs-dcgan-difference
* https://stackoverflow.com/questions/61234271/difference-between-simple-gan-and-dcgan






