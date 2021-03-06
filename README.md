# Custom Land cover classification

This is a code that I wrote and edited for a specific internship task. I had taken ideas from various approaches and papers. In one of my previous repos,[Land Cover Classification on DeepSat](https://github.com/nikjohn7/DeepSat-Land-cover-classification-), I modified a pre-existing notebook and used it to train images from the DeepSat dataset. But one drawback was that the data had already been converted into csv format from MAT format. But if I wanted to test it with real images, it would be a tedious process to configure each image into a csv with requisite features.

So I wrote a much simpler approach, wherein we directly convert a jpg image into a numpy array and then pass them into a neural network to be trained. Thus, implementing this to test on images would be much simpler.

## Dataset

The dataset can be accessed from the `data.zip` file

#### Folders:
- `TRAIN`: Contains 10k images of size 64x64 belonging to 10 classes
- `TRAIN2`: Contains another 10k images similar to previous folder. I only split them into 2 folders, because loading 2 smaller folders from google drive is faster on Colab
- `y_train.npy`: Numpy array containing the class that each image belongs to. It is of size 20k (for the 20k images in the above 2 folders)


## Sample images in dataset

![landcover](https://user-images.githubusercontent.com/29889429/88455553-d5c20c80-ce93-11ea-9545-9711b8cf89eb.jpg)

## Classification classes

| CLASS NAME | NUMPY REPRESENTATION (one-hot) | CLASS NUMBER |
| :----:| :----: | :----: |
| AnnualCrop | [1. 0. 0. 0. 0. 0. 0. 0. 0. 0.] | 0 |
| Forest | [0. 1. 0. 0. 0. 0. 0. 0. 0. 0.] | 1 |
| HerbaceousVegetation | [0. 0. 1. 0. 0. 0. 0. 0. 0. 0.] | 2 |
| Highway | [0. 0. 0. 1. 0. 0. 0. 0. 0. 0.] | 3 |
| Industrial | [0. 0. 0. 0. 1. 0. 0. 0. 0. 0.] | 4 |
| Pasture | [0. 0. 0. 0. 0. 1. 0. 0. 0. 0.] | 5 |
| PermanentCrop | [0. 0. 0. 0. 0. 0. 1. 0. 0. 0.] | 6 |
| Residential | [0. 0. 0. 0. 0. 0. 0. 1. 0. 0.] | 7 |
| River | [0. 0. 0. 0. 0. 0. 0. 0. 1. 0.] | 8 |
| SeaLake | [0. 0. 0. 0. 0. 0. 0. 0. 0. 1.] | 9 |


## Notebook info
I've used Keras with Tensorflow backend to train this model. Feel free to clone/fork and make changes.

You can run the notebook locally or access my [Colab Notebook](https://colab.research.google.com/drive/1aofzD9ssXjT8fuEYaQRBnZFqFPMErp3t?usp=sharing)
