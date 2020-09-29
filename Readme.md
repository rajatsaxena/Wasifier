- `ACGbasedClassifier.ipynb`: deep linear neural network built using 3second 50bins dataset. Reaches testing accuracy ~80%

- `WFbasedClassifier.ipynb`: convolutional neural network built using 32 channels selected from the probe. 82-length waveforms. Reaches testing accuracy ~89%

- `MergedClassifier.ipynb`: merging the above two models using three methods with their results described in the table below

	- 'Multiplication': output probabilities from each model multiplied and the multiplied values are then used for prediction

	- 'Integrated_Trained': output from penultimate layer of individual model fed into a fully-connected (FCN) layer with 8 nodes followed by another FCN layer of 2 nodes. All layers of the merged neural network were set as **trainable**

	- 'Integrated_Frozen': output from penultimate layer of individual model fed into a fully-connected (FCN) layer with 8 nodes followed by another FCN layer of 2 nodes. All layers of the merged neural network were **frozen** except the last two newly added FCN layers. 
