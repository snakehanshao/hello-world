<h1>使用的库如下：</h1>

<blockquote>
  <p>from keras.models import *</p>
  
  <p>from keras.layers import *</p>
  
  <p>from keras.applications import *</p>
  
  <p>from keras.preprocessing.image import *</p>
  
  <p>import numpy as np</p>
  
  <p>import h5py</p>
  
  <p>from sklearn.utils import shuffle</p>
  
  <p>import pandas as pd</p>
</blockquote>

2、机器硬件配置如下：
使用的是AWS平台上p3.2xlarge实力，具体配置为：8个虚拟GPU，64G内存
3、机器操作系统是Ubun
4、训练时间如下：
（1）本项目主要耗时的是提取特征向量，时间如下所示，其中没两行时间代表提取一个Keras模型所花费的时间
Found 25000 images belonging to 2 classes.
Found 12500 images belonging to 1 classes.
2000/2000 [==============================] - 573s 287ms/step
500/500 [==============================] - 133s 266ms/step
Found 25000 images belonging to 2 classes.
Found 12500 images belonging to 1 classes.
2000/2000 [==============================] - 237s 119ms/step
500/500 [==============================] - 48s 96ms/step
Found 25000 images belonging to 2 classes.
Found 12500 images belonging to 1 classes.
2000/2000 [==============================] - 234s 117ms/step
500/500 [==============================] - 48s 96ms/step
Found 25000 images belonging to 2 classes.
Found 12500 images belonging to 1 classes.
2000/2000 [==============================] - 253s 127ms/step
500/500 [==============================] - 51s 103ms/step
Found 25000 images belonging to 2 classes.
Found 12500 images belonging to 1 classes.
2000/2000 [==============================] - 259s 129ms/step
500/500 [==============================] - 53s 105ms/step
Found 25000 images belonging to 2 classes.
Found 12500 images belonging to 1 classes.
2000/2000 [==============================] - 319s 159ms/step
500/500 [==============================] - 66s 132ms/step</p>

<h2>（2）提取完特征向量后，训练所花费的时间就比较少了，如下所示：</h2>

<p>Train on 40000 samples, validate on 10000 samples
Epoch 1/16
40000/40000 [==============================] - 128s 3ms/step - loss: 0.0305 - acc: 0.9912 - val_loss: 0.0094 - val_acc: 0.9974
Epoch 2/16
40000/40000 [==============================] - 9s 231us/step - loss: 0.0109 - acc: 0.9970 - val_loss: 0.0087 - val_acc: 0.9973
Epoch 3/16
40000/40000 [==============================] - 10s 248us/step - loss: 0.0080 - acc: 0.9981 - val_loss: 0.0061 - val_acc: 0.9981
Epoch 4/16
40000/40000 [==============================] - 10s 241us/step - loss: 0.0071 - acc: 0.9980 - val_loss: 0.0054 - val_acc: 0.9981
Epoch 5/16
40000/40000 [==============================] - 9s 233us/step - loss: 0.0057 - acc: 0.9983 - val_loss: 0.0050 - val_acc: 0.9985
Epoch 6/16
40000/40000 [==============================] - 9s 231us/step - loss: 0.0051 - acc: 0.9985 - val_loss: 0.0045 - val_acc: 0.9985
Epoch 7/16
40000/40000 [==============================] - 9s 222us/step - loss: 0.0041 - acc: 0.9988 - val_loss: 0.0040 - val_acc: 0.9987
Epoch 8/16
40000/40000 [==============================] - 9s 225us/step - loss: 0.0038 - acc: 0.9990 - val_loss: 0.0035 - val_acc: 0.9989
Epoch 9/16
40000/40000 [==============================] - 9s 227us/step - loss: 0.0035 - acc: 0.9990 - val_loss: 0.0036 - val_acc: 0.9989
Epoch 10/16
40000/40000 [==============================] - 9s 233us/step - loss: 0.0029 - acc: 0.9992 - val_loss: 0.0034 - val_acc: 0.9990
Epoch 11/16
40000/40000 [==============================] - 9s 235us/step - loss: 0.0028 - acc: 0.9993 - val_loss: 0.0028 - val_acc: 0.9991
Epoch 12/16
40000/40000 [==============================] - 10s 239us/step - loss: 0.0023 - acc: 0.9993 - val_loss: 0.0030 - val_acc: 0.9991
Epoch 13/16
40000/40000 [==============================] - 9s 224us/step - loss: 0.0021 - acc: 0.9995 - val_loss: 0.0026 - val_acc: 0.9993
Epoch 14/16
40000/40000 [==============================] - 9s 220us/step - loss: 0.0020 - acc: 0.9995 - val_loss: 0.0028 - val_acc: 0.9991
Epoch 15/16
40000/40000 [==============================] - 9s 221us/step - loss: 0.0018 - acc: 0.9995 - val_loss: 0.0034 - val_acc: 0.9988
Epoch 16/16
40000/40000 [==============================] - 9s 218us/step - loss: 0.0015 - acc: 0.9996 - val_loss: 0.0022 - val_acc: 0.9993</p>
