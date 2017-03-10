# Occlusion-Aware Face Inpainting with GAN in tensorflow

![](/flowchart.pdf)
+ We modified a few functions in [Brandon Amos' implementation of image completion] (https://github.com/bamos/dcgan-completion.tensorflow)
+ These modifications allows us to detect and reconstruct the occluded regions on human face images.
+ In checkpoint directory, there is a new model pretrained on [CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html). We exclude the faces with glasses attributes in advance in order to generate uncorrupted faces.


