# 17s1-cs9417 Assignment 2
This github repo is created as a part of the [Assignment 2](http://www.cse.unsw.edu.au/~mike/comp9417/ass2_proj.html/) of [COMP9417 Machine Learning and Data Mining](http://www.cse.unsw.edu.au/~cs9417) taught at [Unviersity of New South Wales](https://www.unsw.edu.au)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See Running for notes on how to deploy the project on a live system.

### Prerequisites

Following prerequisites are essential for this code to run.

```
git
python3
pip3
numpy
pandas
matplotlib
tensorflow
```

Following commands are just a reference to install the dependencies on a Ubuntu like linux system. Please refer to their respective websites to properly install the dependencies

```
sudo apt-get install git

sudo apt-get install python3

sudo apt-get install python3-pip

pip3 install numpy

pip3 install pandas

pip3 install matplotlib

pip3 install tensorflow
```

### Installing

A step by step series of examples that tell you have to get a development env running

Once the dependencies are installed, clone this github repository onto your local machine as follows
```
git clone git@github.com:suryaavala/17s1-cs9417.git
```

Then cd into the cloned directory

```
cd 17s1-cs9417
```

## Testing the Installation

Run the following commands to test if the code has been installed properly

```
cd code

python3 mnist_nn.py
```

Expected output
```
You did not run the program as designed
Please run the program again as follows(case sensitive Train!=train):
python3 mnist_nn.py train/predict
Exiting the program...
```
If you see the above output, then the installation is successful

## Running

The code can be run to either Train the classifier or to Predict the results using the pretrained classifier

### Train
Inorder to train the classifier run the following code

```
pwd
```
Make sure your current directory is ```/17s1-cs9417/code/```

```
python3 mnist_nn.py train

```
The classifier takes around ~60min to run on a 1.7GHz Intel Dual Core i7 processor.
During the program execution you'll be seeing something like follows:
```
suryatherisingstar@instance-1:~/17s1-cs9417/dev$ python3 mnist_nn.py train
Extracting data from yann.lecun.com/exdb/mnist/
Successfully downloaded train-images-idx3-ubyte.gz 9912422 bytes.
Extracting MNIST_data/train-images-idx3-ubyte.gz
Successfully downloaded train-labels-idx1-ubyte.gz 28881 bytes.
Extracting MNIST_data/train-labels-idx1-ubyte.gz
Successfully downloaded t10k-images-idx3-ubyte.gz 1648877 bytes.
Extracting MNIST_data/t10k-images-idx3-ubyte.gz
Successfully downloaded t10k-labels-idx1-ubyte.gz 4542 bytes.
Extracting MNIST_data/t10k-labels-idx1-ubyte.gz
Data extracted
step 0, training accuracy 0.16
step 100, training accuracy 0.9
step 200, training accuracy 0.96
step 300, training accuracy 0.96
step 400, training accuracy 0.88
step 500, training accuracy 0.96
step 600, training accuracy 0.92
step 700, training accuracy 0.92
step 800, training accuracy 0.96
step 900, training accuracy 1
step 1000, training accuracy 0.94
....
....
....
```
The training is terminated at step 30000 and you will see something like
```
step 29000, training accuracy 1
step 29100, training accuracy 1
step 29200, training accuracy 1
step 29300, training accuracy 1
step 29400, training accuracy 1
step 29500, training accuracy 1
step 29600, training accuracy 1
step 29700, training accuracy 1
step 29800, training accuracy 1
step 29900, training accuracy 1
test accuracy 0.9927
Model saved in file: ./model/model.ckpt
```
### Predict

Inorder to predict the labels using create a csv like this [test.csv](https://www.kaggle.com/c/digit-recognizer/data) and place it in
```
17s1-cs9417/code/data
```

And then run the following command
```
python3 mnist_nn.py predict
```
Predicted results will be saved in
```
17s1-cs9417/submission_softmax.csv
```

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/suryaavala/17s1-cs9417/tags).

## Authors

* **Surya Avala** - *Initial work* - [SuryaAvala](https://github.com/suryaavala)

See also the list of [contributors](https://github.com/suryaavala/17s1-cs9417/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* [Tensorflow](https://tensorflow.org)
* [Martin Görner](https://twitter.com/martin_gorner)


##### < / > With :heart: Using [Python](https://www.python.org/) and [Tensorflow](https://www.tensorflow.org/)
