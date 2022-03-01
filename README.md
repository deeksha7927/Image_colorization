<div align='center'>
  <h2>Image Colorization With GANs</h2>
  </div>
 


<h3>Description</h3>
  
  </div>
 GANs are the state-of-the-art machine learning models which can generate new data instances from existing ones. They use a very interesting technique, inspired from the Game   Theory, to generate realistic samples.In this project, we'll use GANs to colorize a grayscale ( B/W ) image. In addition to that, our generator model will have a structure similar to that of a UNet i.e the one with skip connections.
 </div>



 <h3>The GAN</h3>
 <div>
  <h4 align="center">A. Generator</h4>
<div>Our generator ( represented as  G  ) will take in grayscale image  x  and produce a RGB image  G(x) . Note,  x  will be a tensor of shape  ( batch size , 120 , 120 , 1 ) and the output  G(x)  will have a shape  ( batch size , 120 , 120 , 3 ) .Our generator will have a encoder-decoder structure, similar to the UNet architecture. Additionally, we use Dilated convolutions to have a larger receptive field.<div>


<h5 align="center">B. Discriminator<h5>
  <div>The discriminator model, represented as  D , will take in the real image  y  ( from the training data ) and the generated image  G(x)  ( from the generator ) to output two probabilities.We train the discriminator in such a manner that is able to differentiate the real images and the generated images. So, we train the model such that  y  produces a output of  1.0  and  G(x)  produces an output of  0.0 .<div>
  </div>
  
  


