# Topic 1:  Convolution

> Convolution is the process of convolving the input matrix ( for example- matrix of pixel wise color values in an rgb image) by a filter matrix (for example - rgb filter kernels to identify rgb color space in the input image).
> So, in a convolutional layer, the filter or kernel is used to extract feature map from the input image by convolving around it starting from top left corner of the input image, where in it multiplies the values in the filter of Receptive Field (3x3) with the original pixel values of the image, in simple words computing element wise multiplication. Then, these multiplications are added up to generate single value. After convolving through whole of input image, by moving 1 step at a time, the feature map is generated.


#### Example-
There is a RGB image 400 x 400 on which convolution is to be done.

Hence, our input matrix becomes (400x400x3)
Filter matrix can be of any dimension, commonly used is 3x3.
So, for our input matrix, filter matrix becomes (3x3x3)

Now in process of convolution, each element of filter matrix is multiplied on the receptive field in input matrix to generate feature map.

In this case, it generates a feature map of dimensions (398x398x3)

![con im.gif](\:storage\0.i939i0hg1ue.gif)

# Topic 2: 1x1 Convolution

> Convolution with kernel of size 1x1 is used in dimension reductionality in the filter dimension. For example, an input image of 400 x 400 with 100 features on convolution with 20 filters of 1x1 would result in 400x400x20.
> Purpose of 1x1 convolution is feature pooling. whereby it sum pools the features of various channels/feature-maps of a given layer. 
> 1x1 convolutional filter behaves exactly the same as normal filter. Only thing is, it does not care about the correlation of information in the same feature map. Meaning, there is no visual pattern being learned in here. Instead, the filter pools the information across multiple feature maps.

![1x1 conv.gif](\:storage\0.xb1rvq1df38.gif)

#### Example -
 There is a RGB image 400 x 400 on which convolution is to be done.

Hence, our input matrix becomes (400x400x3)
Now we apply convolution with 100 filters of 3x3 size.
Our, output matrix becomes 398x389x100. This is lots of pixel points information, and may be we don't need all of it or it's hard to compute further feature map on it.
Hence, to reduce its dimension, one way is to apply convolution of 1x1 20 such filters.
Which in turn gives the output matrix (398x398x20).



# Additional Topic 1 : 10 examples of use of MathJax in Markdown

### Example 1:
For Inline formulas, enclose the formula inside single $ brackets.
Example- 
1. $\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$ 

### Example 2:
For displayed formulas, use double $ brackets.
Example-
1. $$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$ 

### Example 3:
For Greek letters, use syntax ->
&Name-Of-Character; 
Example-
1. For alpha - &alpha;
2. For beta - &beta;
3. For capital gamma, write "Gamma" - &Gamma;
4. For capital delta, write "Delta" - &Delta;

### Example 4:
For superscripts, inside single/double $ bracket and use ^ 
Example-
1. $i^2$

### Example 5:
For subscripts, inside single/double $ bracket and use  _
Example-
1. $log_2 x$

### Example 6:
In Groups, Superscripts, subscripts, and other operations apply only to the next “group”. A “group” is either a single symbol, or any formula surrounded by curly braces {…}
Example-
1. $x_{i^2}$
2. $x^{y^z}$

### Example 7:
For Sums, use \sum inside single/double $ brackets
Example-
1.$\sum_{i=0}^\infty i^2$

### Example 8:
For Integrals, use \int inside single/doube $ brackets
Example-
1. $$\int i^2$$

### Example 9:
For Fractions, use \frac ab or \over inside single/double $ brackets
Example-
1. $\frac ab$
2. $${a+1\over b+1}$$

### Example 10:
For Radical signs, use \sqrt inside single/double $ brackets
Example-
1. $\sqrt{x^3}$
2. $$\sqrt[3]{\frac xy}$$

