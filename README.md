Smart-Manufacturing-Adaptive-Control-Dataset

https://www.kaggle.com/datasets/programmer3/smart-manufacturing-adaptive-control-dataset?resource=download

Comments and thoughts:

Predictive maintenance is always a very interesting field to look at, but there is a lack of public datasets to work on. Here, we tried to use a Kaggle dataset to see if this dataset is vaiable for such EDA.

For the data train/test split, we considered both a “split by machine ID” and a typical random split strategy. Then, we used a RandomForest and an XGBoost to see if it is possible to perform a 3-class classification, where the classes are:

{
    'Needs Maintenance': 1141, 
    'Unstable': 1141, 
    'Stable': 1141
}

This label distribution worries us instantly, as the split is perfectly even. This rarely happens, unless it is a synthetic dataset. Nonetheless, if it is a synthesis dataset, it may still work out.

Unfortunately, after performing the multi-class classification, we got a F1 score of approximately 0.344, which means that it is unable to distingush the classes; the confusion matrix clearly shows that.

Here comes the final check to see if the dataset is even viable; using t-SNE to see if the data are separable in anyway. From the results, it appears that the data is not separable; hence, it would not be possible to perform any valuable classification task for this dataset.

Conclusion and verdict: This dataset is synthetic and cannot be used.