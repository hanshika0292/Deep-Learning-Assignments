# Assignment 3

## Topic 1 - Dilated Convolution
> Dilated convolution is the normal convolution applied to input with defined gaps. Its purpose is to increase global receptive field of the kernel. For a 2D Image, dilation rate = 1 is normal convolution, with dilation rate = 2, it means skipping one pixel value per input and with dilation rate = 4, it means skipping 3 pixel values per input and likewise for dilation rate = 8.

![](https://cdn-images-1.medium.com/max/1200/1*SVkgHoFoiMZkjy54zM_SUw.gif)

> General use case of dilated convolution process is in Image segmentation, where each pixel is labelled by its corresponding class, this way it keeps the resolutions high. Other cases where its used are in WaveNet (text-to-speech) and ByteNet learn time text translation, where it helps to capture global view of input with less number of parameters. And thus its used in following cases-
> 1. Detection of fine-details by processing inputs in higher resolutions
> 2. Borader view of the input to capture more contextual information
> 3. Faster run-time with less parameters.


## Topic 2 - Depthwise Seperable Convolution
> Depthwise Seperable Convolution will perform spatial convolution while keeping the channels seperate and then follow with a depthwise convolution.
> For Example: We have 3x3 convolutional layer on 16 input channels and 32 output channels. Now, these 16 input channels will be traversed by 32 3x3 kernels resulting in 512(16x32) feature maps. Next, we merge 1 feature map out of every input channel by adding them up, thus getting 32 output channels.
> Now, in DepthWise Seperable Convolution will traverse 16 input channels with 1 3x3 kernel each, giving us 16 feature maps. Now, before merging anything, we traverse these 16 feature maps with 32 1x1 convolutions each and only then start to them add together. This results in 656 (16x3x3 + 16x32x1x1) parameters opposed to the 4608 (16x32x3x3) parameters from above. In this example, depth multiplier is 1.

![](http://tvmlang.org/images/depthconv_tutorial/conv_and_depthconv.png)


## Topic 3 - Strides
> Stride is the number of pixels with which we slide our filter, horizontally or vertically. In a normal convolution with stride 1, we moved our filter one pixel at each step to calculate the output. However, in case of stride 2, we calculate the output for every other pixel, by jumping 2 pixels and as a contrary the output of the convolution would be roughly half the size of the input image.

![](http://machinelearninguru.com/_images/topics/computer_vision/basics/convolutional_layer_1/stride1.gif)

![](http://machinelearninguru.com/_images/topics/computer_vision/basics/convolutional_layer_1/stride2.gif)

> Stride basically controls how the filter convolves around the input volumne. Hence, commonly used when receptive fields are required to overlap less and smaller spatial dimensions are needed.





