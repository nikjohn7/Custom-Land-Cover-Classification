# Custom Land cover classification

This is a code that I wrote and edited for a specific internship task. I had taken ideas from various approaches and papers. In one of my previous repos,[Land Cover Classification on DeepSat](https://github.com/nikjohn7/DeepSat-Land-cover-classification-), I modified a pre-existing notebook and used it to train images from the DeepSat dataset. But one drawback was that the data had already been converted into csv format from MAT format. But if I wanted to test it with real images, it would be a tedious process to configure each image into a csv with requisite features.

So I wrote a much simpler approach, wherein we directly convert a jpg image into a numpy array and then pass them into a neural network to be trained. Thus, implementing this to test on images would be much simpler.

## Dataset

You can download the data set from [here](https://pip.pypa.io/en/stable/)

**Files to download:**

- `TRAIN`: Contains 20k images (28x28) belonging to 10 classes
- `y_train.npy`: A numpy array of size 20k containing corresponding labels of the images in TRAIN folder
- `TEST`: I haven't used this folder in this project, since the labels were not available for the images in this folder. However, you can make use of it by hand labelling all images in the folder. It contains 7k images (28x28)

## Sample images in dataset

![landcover](https://user-images.githubusercontent.com/29889429/88455553-d5c20c80-ce93-11ea-9545-9711b8cf89eb.jpg)

## Notebook info
I've used Keras with Tensorflow backend to train this model. Feel free to clone/fork and make changes.

You can run the notebook locally or access my [Colab Notebook](https://colab.research.google.com/drive/1aofzD9ssXjT8fuEYaQRBnZFqFPMErp3t?usp=sharing)
