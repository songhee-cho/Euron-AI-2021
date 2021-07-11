## Last Time: lots of computer vision tasks

### semantic segmentation

- combining aspects of a semantic segmentation and object detection, the goal is to detect all the instances of the categories, label the pixels belonging

### classification + localization

- in addition to a class label, you also want to draw a box or perhaps several boxes in the image
- where the distinction here is that, in a classification plus localization setup
- you have some fix number of objects that you are looking for
- so, we also saw that this type of paradigm can be applied to the things like pose recognition, where you want to regress to different # of joints in the human body

### object detection

- you start with some fixed where you start with some fixed set of category labels that you are interested in
- and then the task is to draw a boxes around every instance of those objects that appear in the input image.
- and object detection is really distinct from classification plus localization because with object detection, we don't know ahead of time, how many object instances we're looking for in the image.

### instance segmentation

- combining object detection and semantic segmentation

## What's going on inside ConvNets?

- how to stitch up different types of architectures to attack different problems
- ConvNets as a little bit of a black box
- where some input image of raw pixels is coming in on one side.
- It goes to the many layers of convolution and pooling in different sorts of transformations and pooling in different sorts of transformations.
- **outside**: we end up with some set of class scores or some types of understandable interpretable output.
- How ConvNets are working?
- what types of things in the image they are looking for?

### AlexNet

- one relative simple thing is the first layer
- the 1st convolutional layer consists of a # of convolutional filters
- each convolutional of filter has shape 3 by 11 by 11.
- And these convolutional filters gets slid over the input image.
- we take inner products between some chunk of the image.
- and the weights of the convolutional filter
- in AlexNet then we have 64 of these filters
- in a direct inner product between the weights of the convolutional layer and the pixels of the image.
- these filters are looking for by simply visualizing the learned weights of these filters
- lot of things looking for oriented edges
- in various angles and various angles and various positions
- opposing colors
- why does visualizing the weights of the filters?
- Tell you what the filter is looking for
- So this intuition comes from sort of template matching and inner products.
- that if you imagine you have some, some template vector → compute a scalar output by taking inner product between your template vector and some arbitrary piece of data
- then, the input which maximizes that activation
- under a norm constraint on the input is exactly when those two vectors match up
- whenever you are taking inner products, the thing causes an inner product to excite maximally is a copy of the thing you are taking an inner product with.
- → that's why we can actually visualize these weights

### visualize the filters, kernels(raw weights)

- the first layer is 7 by 7 convolution 16 filters
- after the top visualizing the first layer weights

## last layer

- 1000 class scores that are telling us what are the predicted scores for each of the classes in out training data set and immediately before the last layer
- In the case of AlexNet, we have some 4096-dimensional features representation of our image that then gets fed into that final out final layer to predict our final class scores

### Nearest Neighbors

- nearest neighbor classifier
- where we were looking at nearest neighbors in pixels space between CIFAR 10 images
- looks quite similar to the query image

## Texture Synthesis

- input patch → output으로 bigger image with the same texture
- a lot of classical algorithm without neural net

### nearest neighbor

### gradient ascend

- 2015 paper
- concept of gram matrix
- two different feature vectors → C by C matrix
- using true covariance matrices also works but it's a little bit more expensive to compute
- so, in practice a lot people just use this gram matrix descriptor

## Neural Texture Synthesis

- now once we have this sort of neural descriptor of texture
- then we use a similar type of gradient ascent procedure to synthesize a new image that matches the texture of the original image
- feature reconstruction
- to reconstruct the whole feature map from the input image
- reconstruct this gram matrix texture descriptor of the input image instead
- for feature inversion, people wil use the VGG networks for this
- you'll take your texture image, and feed it through the VGG network, compute the gram matrix and many different layers of this network
- then you'll initialize your new image from some random initialization
- and then it looks like gradient ascent again
- use 4 GPU, expensive to compute
- DeepDream
- **problem**: style transfer requires many forward, backward passes through VGG; very slow
- **solution**: train another neural network of perform style transfer for us
- → *fast style transfer*: fix some style that we care about at the beginning

### Fast Style Transfer

1) Train a feedforward network for each style

2) Use pretrained CNN to compute same losses as before

3) After training, stylize images using a single forward pass

- rather than running a separate optimization procedure for each image that we ant to synthesize instead we're going to train a single feed forward network that can input the content image and then directly output the stylized result
- run in real-time이 가능
- have bath normalization
- blend of style이 가능한 경우도 존재

## Summary

- many methods for understanding CNN representations
- **activations**: nearest neighbors, dimensionality reduction, maximal patches, occlusion
- **gradients**: saliency maps, class visualization, fooling images, feature inversion
- **fun**: DeepDream, Style Transfer
