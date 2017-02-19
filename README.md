# Picture Quest
Interactive game that uses AI to fill an object list
Uses Tensorflow + Python + Web Server

### Requirements 
[Tensorflow](https://www.tensorflow.org/)

[Python](https://www.python.org/)

[Pip](https://pip.pypa.io/en/stable/installing/#do-i-need-to-install-pip)


### Getting Started!

Clone This Proyect
(In Terminal or Desktop App)
```
git clone https://github.com/AxelAli/Picture-Quest.git
```

Install Dependencies for The Image Downloader (Optional, Makes it easier to download)
(In Terminal)
```
sudo pip install BeautifulSoup bs4 requests 
```



### Getting Started! Pt.2


Start Docker! (in proyect folder)
```
docker run -it -v $HOME/Picture-Quest:/Picture-Quest  gcr.io/tensorflow/tensorflow:latest-devel
```

Use the following command to install latest Tensorflow package
```
sudo pip install tensorflow --upgrade
```

Now. (Just in case)
```
cd ..
cd ..
cd /tensorflow
git pull
```
####Optional (Getting a dataset)
Great!
We have 2 Python scripts to download images from google.

#####With "user interface"
```
python GetImagesfromgoogle.py
```
We get the following Question:
```
What do i search for?
```

Here you can write anything you want, (Ex. Dog,Car,Flower).

You can also add extra words to be more especific or to get a wider dataset (Ex. White Dog,Ferrari Car, Sun Flower).

The terminal will start to output each image downloaded 

```
there are total 100 images
1
2
3
4
5
[...]
```
#####With console commands
```
python GetImagesfromgoogleCommand.py
```
How do i use it?
Easy, just write after GetImagesfromgoogleCommand.py you query
```
python GetImagesfromgoogleCommand.py QUERY
```
Ex.
```
python GetImagesfromgoogleCommand.py Dog
```

You can also "Batch download" 
```
python GetImagesfromgoogleCommand.py DOG
python GetImagesfromgoogleCommand.py CAT
python GetImagesfromgoogleCommand.py PARROT
python GetImagesfromgoogleCommand.py RAT
```
Now you can let it download overnight


Your folder will look like this:

![](http://i.imgur.com/mrRnC2F.png)

NOTE:All downloads are in the data folder, there is also a folder for each query.

####Lets Train!
Just Run the following commands

```
python image_retraining/retrain.py --bottleneck_dir=/data/bottlenecks --how_many_training_steps 1000  --model_dir=/data/inception --output_graph=/data/retrained_graph.pb --output_labels=/data/retrained_labels.txt --image_dir ./data/
```
#####What are these arguments?
**--bottleneck_dir :**


///WIP - WORK IN PROGRESS
