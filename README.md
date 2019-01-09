In this repo you can find jupyter notebook with code which I used to train neural network in [HackerEarth Deep Learning Challenge 2](https://www.hackerearth.com/practice/machine-learning/challenges-winning-approach/deep-learning-challenge-two/tutorial/). 

During the challenge I had to identify the class of thorax diseases from the given chest x-ray images.
My trained neural network took 2nd place.

#### Tools
 - jupyter notebook,
 - keras,
 - pandas,
 - numpy,
 - sklearn
 
#### Data
In machine learning the most important thing is to search all data which you can use to train your model. 
So I did my homework and searched on the net all lungs X-ray images. 
Besides data available in HackerEarth datasets I've used additional ones which I found on the [web](http://academictorrents.com/details/557481faacd824c83fbf57dcf7b6da9383b3235a). 
I also generated 10k images for classes which have smallest number of images. 


#### How I trained my network
I used transfer learning. 

Firstly I imported ResNet50 architecture with imagenet weights. I frozen all layers except full connected layer. 
I ran 20 epochs with optimizer _Adam(0.0001, decay=0.00001)_. Then I unfrozen last 35 layers and ran 20 epochs with optimizer _Adam(0.0001, decay=0.00000001)_.
I used _AWS p2.xlarge_ architecture to train my model.

