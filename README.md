
# deepdream 
This repository contains implementation of deepdream in pytorch. deepdream helps us to 
visualize what the neuron or one of the layer of a deep neural network is actually looking. 
## Algorithm

We generally take a pretrained neural network and then select a random layer from it. In it we have to 
amplify the output from that particular layer, which we do by applying gradient ascent.

![image](https://user-images.githubusercontent.com/76916164/132575227-66bda8b3-3432-42db-aaee-bfa8e4219e12.png)
![image](https://user-images.githubusercontent.com/76916164/132576082-fc5ab9b8-fb6e-4b6d-a2ae-f5a51dfedb25.png)
![image](https://user-images.githubusercontent.com/76916164/132576122-a4d9a1a2-1070-4240-9192-3dbbebe2f67a.png)
![image](https://user-images.githubusercontent.com/76916164/132576142-ecfdead5-3e32-4a6c-b6db-7306a68643dc.png)


In implementing deepdreams, we initially apply deepdream on a downsampled low resolution formats of the original image
after which we gradually increase the resoultion of the downsampled image, stacking the previous image on top and applying deepdream at every step, untill
we got out final highest resoulution image. This is called image pyramid, and by doing this, the network will see different resolutions each time and can focus on coarse features of the image at one and the texture of the image at the other.

## Results
By twitching different models, layers, image pyramid size many different types of images can be created. Here are some examples.
![Toucan](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Original%20Images/Toucan.jpg)
![processed_toucan](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Processed%20Images/processed_toucan.png)


![processed_sky-dd](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Processed%20Images/processed_sky-dd.png)


![processed_daali](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Processed%20Images/processed_daali.png)


![processed_wave](https://github.com/Sandstorm831/Deep-Dreams/blob/main/Processed%20Images/processed_wave.png)


