# Project Results

## Major issues with GANs

#### Non-convergence
Non-convergence occurs when the model parameters oscillate, destabilize and never converge.

#### Mode collapse
Mode collapse occurs when  the discriminator is too harsh and causes the generator to produce a limited variety of sample.

#### Diminished gradient
The discriminator gets too successful that the generator gradient vanishes and learns nothing.


## Results

### Original images from dataset
|  ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original1.png "original_Image1") | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original2.png "original_Image2")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original3.png "original_Image3")  | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original4.png "original_Image4")  |
| ------- |:-------------:| :-------:| ----------:|
| ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original5.png "original_Image5")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original6.png "original_Image6")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original7.png "original_Image7")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/originals/original8.png "original_Image8")   |


### Generated images without modifications
|  ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_0.png "original_Image1") | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_11.png "original_Image2")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_13.png "original_Image3")  | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_36.png "original_Image4")  |
| ------- |:-------------:| :-------:| ----------:|
| ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_66.png "original_Image5")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_83.png "original_Image6")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_183.png "original_Image7")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_no_changes/50000_248.png "original_Image8")   |

### Generated images with FID = 110
|  ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_124.png "tweaked_Image1") | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_131.png "tweaked_Image2")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_133.png "tweaked_Image3")  | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_138.png "tweaked_Image4")  |
| ------- |:-------------:| :-------:| ----------:|
| ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_149.png "tweaked_Image5")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_153.png "tweaked_Image6")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_156.png "tweaked_Image7")   | ![alt text](https://github.com/pejner/keras-gan/blob/master/images/output_with_tweaking/50000_157.png "tweaked_Image8")   |












