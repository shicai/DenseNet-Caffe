# DenseNet-Caffe

### Introduction
We manually converted the original torch models into caffe format from https://github.com/liuzhuang13/DenseNet.

For details of these networks, please read the original paper:
- [Densely Connected Convolutional Networks](https://arxiv.org/abs/1608.06993)


### Pretrained DenseNet Models on ImageNet

The top-1/5 accuracy rates by using single center crop (crop size: 224x224, image size: 256xN)

Network|Top-1|Top-5|Download|Architecture
:---:|:---:|:---:|:---:|:---:
DenseNet 121 (k=32)| 74.91| 92.19| [caffemodel (30.8  MB)](https://drive.google.com/open?id=0B7ubpZO7HnlCcHlfNmJkU2VPelE)| [netscope](http://ethereon.github.io/netscope/#/gist/4928834eca7f06261ba0558e0ff63a6a)
DenseNet 169 (k=32)| 76.09| 93.14| [caffemodel (54.6  MB)](https://drive.google.com/open?id=0B7ubpZO7HnlCRWVVdUJjVVAyQXc)| [netscope](http://ethereon.github.io/netscope/#/gist/71335b6e8634327c9b9216619572b3dd)
DenseNet 201 (k=32)| 77.31| 93.64| [caffemodel (77.3  MB)](https://drive.google.com/open?id=0B7ubpZO7HnlCV3pud2oyR3lNMWs)| [netscope](http://ethereon.github.io/netscope/#/gist/ee808e19615844b8dbc7b13e92abd233)
DenseNet 161 (k=48)| 77.64| 93.79| [caffemodel (110 MB)](https://drive.google.com/open?id=0B7ubpZO7HnlCa0phRGJIRERoTXM)| [netscope](http://ethereon.github.io/netscope/#/gist/8fae97d9c66b40b8da443f7f23e9b29b)

**Update** (July 27, 2017): for your convenience, we also provide a link to these models on [Baidu Disk](https://pan.baidu.com/s/1gfjD8cF).

### Notes
Due to compatibility reasons, several modifications have been made:
- BGR mean values **[103.94,116.78,123.68]** are subtracted
- **scale: 0.017** is used, instead of the original std values for image preprocessing
- **ceil_mode: false** is used in the first pooling layers ('pool1') 
