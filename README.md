# Occlusion-Aware Face Inpainting with GAN in tensorflow


![](/flow_chart.png)


+ We modified a few functions in [Brandon Amos' implementation of image completion] (https://github.com/bamos/dcgan-completion.tensorflow)
+ These modifications allows us to detect and reconstruct the occluded regions on human face images.
+ In checkpoint directory, there is a new model pretrained on [CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html). We exclude the faces with glasses attributes in advance in order to generate uncorrupted faces.


Modification
------------
+ Added arguments in `complete.py`, such as the parameters of calculating new masks, the number of iterations that is needed to  update masks, etc.  
+ Modified complete function in `model.py` and implemented the calculation of new masks.
+ Implemented [Adam](https://arxiv.org/abs/1412.6980) optimizer

Additional Requirement 
-----------
+ [scikit image](http://scikit-image.org/)

	`$ pip install scikit-image`

Usage
-----------
Almost the same as that in [Brandon Amos' blog](https://bamos.github.io/2016/08/09/deep-completion/).

The flow should be:
+ First, aligning face images with [OpenFace](http://cmusatyalab.github.io/openface/setup/) 
+ Then, training GAN with aligned images.
+ Synthesize inpainted images as our output results.

Some example results:
![](/example_result.png)


