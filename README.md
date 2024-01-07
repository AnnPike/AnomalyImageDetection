# AnomalyImageDetection

The attached dataset contains 100 images, 90 of them belong to MNIST (half are ‘1’
digit and the other half are ‘2’).
The remaining 10 images are ‘1’ and ‘2’ digits taken from SVHN dataset.
The goal is to detect these anomalous images.
![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/dataset.png)
First, I investigate the dataset in the notebook 1EDA
My idea is to build a simple neural network for MNIST dataset (implemented in 2simpleNNpretrainMNIST notebook), and then use the last layer as embedding for each image. Then I work with these embedding vectors. I use dimensionality reduction to visualize the samples and chose to use clustering because the anomalous images form a clear cluster:
![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/clustering.png)
I plot the images of each cluster and obtain perfect results where one of the clusters contains all anomalous images, whereas other clusters represent numbers 1 and 2 from MNIST dataset.
![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/anomaly_cluster.png)
