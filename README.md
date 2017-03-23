# Testing wavenet generation.

Before you start you might want to start downloading the training data set, at the typing of this guide it's about 16Gb of data found at [Corpus](http://homepages.inf.ed.ac.uk/jyamagis/release/VCTK-Corpus.tar.gz)

## Installation
Start of by installing the required package handler.
```
sudo apt install python-pip
```

We need the code from the repository
```
git clone https://github.com/ibab/tensorflow-wavenet.git
```

Then we need to install the python packages required, the requirements.txt is found in the repository.
```
pip install numpy
pip install -r requirements.txt
pip install tensorflow
```

## Train your model

In order to train the model you want to point the training script to your corpus directory and then add a silence_threshold lower than 0.3 which is default. The training data have some really low volume samples that you want to train your model on. With a threshold of 0.3 you'll get hundreds of files that is ignored.
```
python train.py --data_dir=corpus --silence_threshold 0.1
```



# Windows
In your mingw32
```
https://github.com/xianyi/OpenBLAS.git
cd [dir]
make
make install
```

Download libraries for intel processors with mingw at [here](http://icl.cs.utk.edu/lapack-for-windows/lapack/#libraries_mingw)

```
mingw32-make blaslib
mingw32-make cblaslib
mingw32-make lapacklib
mingw32-make lapackelib
mingw32-make
```
