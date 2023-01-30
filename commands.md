# Commands

All commands are executed from the `darknet` directory.

## Video Detection using pre-trained weights

```
./darknet.exe detector demo ./cfg/coco.data ./cfg/yolov4.cfg ../yolov4.weights -ext_output '../../OneDrive - EPITA/Ing3/DNN - Deep Neural Network/IMG_1688.MOV' -out_filename res.mp4
```

## Training

```
./darknet.exe detector train ../cfg/mnist.data ../yolov4_custom.cfg ../yolov4.conv.137 -map
```

## Image Detection using trained weights

```
./darknet.exe detector test ../cfg/mnist.data ../yolov4_custom.cfg ./backup/yolov4_custom_last.weights
```

## Using a file list as input

```
cat ../cfg/mnist_test.txt | ./darknet.exe detector test ../cfg/mnist.data ../yolov4_custom.cfg ./backup/yolov4_custom_best.weights
```
