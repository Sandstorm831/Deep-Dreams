
# deepdream 
This repository contains implementation of deepdream in pytorch. deepdream helps us to 
visualize what the neuron or one of the layer of a deep neural network is actually looking. 
## Algorithm

We generally take a pretrained neural network and then select a random layer from it. In it we have to 
amplify the output from that particular layer, which we do by applying gradient ascent.

![image](https://user-images.githubusercontent.com/76916164/132575227-66bda8b3-3432-42db-aaee-bfa8e4219e12.png)

In implementing deepdreams, we initially apply deepdream on a downsampled low resolution formats of the original image
after which we gradually increase the resoultion of the downsampled image, stacking the previous image on top and applying deepdream at every step, untill
we got out final highest resoulution image. This is called image pyramid, and by doing this, the network will see different resolutions each time and can focus on coarse features of the image at one and the texture of the image at the other.

## Results
By twitching different models, layers, image pyramid size many different types of images can be created. Here are some examples.
![Toucan](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Original%20Images/Toucan.jpg)
![processed_toucan](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Processed%20Images/processed_toucan.png)

