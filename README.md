# Image-colorization-GAN

## Description

This Project is implementation of image colorization from black and white images using GAN.

## Libraries

- TensorFlow
- sklearn
- PIL
- matplotlib
- numpy

## Dataset

The dataset used to train this model is : https://www.kaggle.com/datasets/jessicali9530/stl10/data

### Custom dataset
To use custom dataset ensure you create a folder `data` which has all the coloured images.

## Training 
### Config
```python
batch_size = 4
img_size = 120
dataset_split = 2500
master_dir = 'data/'
```
### Epochs: 200

### Total training time: 6867.23 seconds

## Using model

To use the model you can directly use the model from the repo `generator.keras` which outputs colourized image when black and white image is provided.

### Example:

```python
generator = tf.keras.models.load_model('generator.keras')
# Generate output for the test_x data
y = generator( test_x[0:10] ).numpy()
```
