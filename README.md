# Intro

In this project next pretrained classification models was used:
 
 - VGG16
 - InceptionResNetV2
 - Xception
 - ResNeXt50

In our examples we will use two sets of pictures, which we got from [Kaggle](https://www.kaggle.com/c/dogs-vs-cats/data), 
1000 cats and 1000 dogs (although the original dataset had 12,500 cats and 12,500 dogs, we just took the first 1000 images for each class).
We also use 400 additional samples from each class as validation data. To make fair evaluation of our model we use 200 images for each class as test sample.


### Result we have got

| Model     | Total number of parametrs |      Accuracy, %       | 
|-----------|:-------:|:----------------------------:|
| VGG16  |23 103 809 | 97.0 | 
| InceptionResNetV2  | 68 493 282| 94.5| 
| Xception  | 54 416 682| 98 | 
| ResNeXt50 |  |  | 


# Usage

### Arguments

`model_name` - you can choose one of 4 models: VGG16, InceptionResNetV2, Xception, ResNeXt50 <br>
`train_data_dir` - path to train set <br>
`validation_data_dir` - path to validation set <br>
`test_data_dir` - path to test set<br>
`output_path_for_model` - use yout working directory <br>
`output_path_for_prediction` - path to save model prediction <br>
`source_path_for_actual_class` - pictures and actual classes map for train set <br>

`nb_train_samples` - number of train samples <br>
`nb_validation_samples` - number of validation samples <br>
`nb_test_samples` - number of test samples <br>
`epochs` = number of epochs <br>
`batch_size` = batch_size <br>
`img_width` = target size of image <br>
`img_height` = target size of image <br>

It's recommended to use `epochs` = 100, `batch_size` = 8, `img_width`, `img_height` = 256

### Directories

```
   train/
        dogs/
            dog001.jpg
            dog002.jpg
            ...
        cats/
            cat001.jpg
            cat002.jpg
            ...
   validation/
        dogs/
            dog001.jpg
            dog002.jpg
            ...
        cats/
            cat001.jpg
            cat002.jpg
            ...
   test/
            dog001.jpg
            dog002.jpg
            ...
            cat001.jpg
            cat002.jpg
  
```
  
  
```
python3 comparison_of_models.py --model_name MODEL_NAME --train_data_dir TRAIN_DATA_DIR --validation_data_dir VALIDATION_DATA_DIR--test_data_dir TEST_DATA_DIR--output_path_for_model OUTPUT_PATH_FOR_MODEL--output_path_for_prediction OUTPUT_PATH_FOR_PREDICTION--source_path_for_actual_class SOURCE_PATH_FOR_ACTUAL_CLASS--nb_train_samples NB_TRAIN_SAMPLES--nb_validation_samples NB_VALIDATION_SAMPLES--nb_test_samples NB_TEST_SAMPLES--epochs EPOCHS--batch_size BATCH_SIZE--img_width IMG_WIDTH --img_height IMG_HEIGHT

```
