# CNN using Resnet34 Architecture

1. Used fastai library on top of PyTorch.
2. Refer to [`Deeper_Systems_CNN.ipynb`](https://github.com/sachinchaturvedi93/deepersystems-cnn/blob/master/Deeper_Systems_CNN.ipynb) file for model building and details.
3. [`test.preds.csv`](https://github.com/sachinchaturvedi93/deepersystems-cnn/blob/master/test.preds.csv) contains the predictions of labels for the test set.
4. [`test_new.zip`](https://github.com/sachinchaturvedi93/deepersystems-cnn/blob/master/test_new.zip) test images that have been rotated to **upright** position.

## Short Description

Loaded the train images with the labels from the train.truth.csv file and kept aside a validation set(20% of the data). Used CNN with pretrained resnet34 architecture to first train the outer layers with our given data and then unfreezing the model and trained it more on all the layer. Used callback function to used the best model out of the 10 epochs we chose. Once the model was selected, we saved it and exported it. We then opened up a random image fron the test and checked our prediction if it was it was labelled correctly and it was. Then we applied it on the whole test set and saved our predictions in a csv file. Finally, we used the PIL library to rotate images based on our labels. e.g., If an image was upside down then we rotated it by 180 degress to make it upright. After this we saved the folder into an archive. 

