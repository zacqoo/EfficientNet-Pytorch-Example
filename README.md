# EfficientNet-Pytorch

PyTorch implementation of [EfficientNet](https://github.com/lukemelas/EfficientNet-PyTorch).

## Step 1：Prepare dataset
---
Then the data directory should looks like:   
```
-dataset\
    -model\
    -train\
        -class_1\
        -class_2\
        ...
    -test\
        -class_1\
        -class_2\
        ...
```

## Step 2: Install required Python packages

`pip install -r requirements.txt`

## Step 3: run train and test 

```
python efficientnet_train.py --data-dir "/full-path/to/EfficientNet-Pytorch-Example/dataset" --num-epochs 500 --batch-size 8 --img-size 1024  --class-num 4 --lr 0.005 --net-name "efficientnet-b5"
```

The final results and the best model will be saved in ```dataset/model/```.

### Optional details

```--data-dir``` : (str) Path of ```/dataset``` folder. Default: ```None```

```--num-epochs``` : (int) Number of epochs for training. Default: ```40```

```--batch-size``` : (int) Batch size. Default: ```4```

```--img-size``` : (int) Selected size for image to be resized. Default: ```[1024,1024]```

```--class-num``` : (int) Number of classes in dataset. Default: ```3```

```--weights-loc``` : (str) Path of weights to be loaded. If None, pretrained weights will automatically be downloaded & loaded. Default: ```None``` Example: ```"...//weights.pth//"``` 

```--lr``` : (float) Learning rate. Default: ```0.01```

```--net-name``` : (str) States which efficientnet model will be used. Used for downloading pretrained weights as well.

```--resume-epoch``` : (int) Defines starting epoch. Default: ```0```

```--momentum``` : (float) Sets momentum. Default: ```0.9``` 
 
The pre-trained model is available on >[release](https://github.com/lukemelas/EfficientNet-PyTorch/releases). 
