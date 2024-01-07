# AnomalyImageDetection

The attached dataset contains 100 images, 90 of them belong to MNIST (half are ‘1’ digit and the other half are ‘2’). The remaining 10 images are ‘1’ and ‘2’ digits taken from SVHN dataset. The goal is to detect these anomalous images.<br />
![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/dataset.png)<br />
First, I investigate the dataset in the notebook ```1EDA.ipynb``` <br />
My idea is to build a simple neural network for MNIST dataset (implemented in ```2simpleNNpretrainMNIST.ipynb ``` notebook), and then use the last layer as embedding for each image. <br />
Then I work with these embedding vectors in ```3get_embeding_and_predict.ipynb```. I use dimensionality reduction to visualize the samples and chose to use clustering because I suspect, that the anomalous images form a cluster:<br />
![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/clustering.png)<br />
I plot the images of each cluster and obtain perfect results where one of the clusters contains all anomalous images, whereas other clusters represent numbers 1 and 2 from MNIST dataset.<br />
![alt text](https://github.com/AnnPike/AnomalyImageDetection/blob/main/anomaly_cluster.png)

*Note, the trained NN is not added to GitHub because it is larger than GitHib allows
