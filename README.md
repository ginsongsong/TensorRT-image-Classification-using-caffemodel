# TensorRT-image-Classification-using-caffemodel
TensorRT4.0 image classification using caffemodel

Use TensorRT to Calculate the ROC or confusion matrix for diff precision INT8/FP16/FP32 classification.

How to install
```
make
```

You can simply add the test list to giexec.
```
giexec --deploy=deploy.prototxt --model=xx.caffemodel --label=label.txt --test=test.txt

model: IcepV3.caffemodel
deploy: deploy.prototxt
output: loss3/prob
fp16
test: T.txt
Input "data": 1x256x256
Output "loss3/prob": 2x1x1
File:T.txt
Success to decode image
Dim0: 1 Dim1:1024 Dim2:1024
name=data, bindingIndex=0, buffers.size()=2
Memory Read...Image Ok
Average over 1 runs is 8.40288 ms (percentile time is 8.40288).
name=loss3/prob, bindingIndex=1, buffers.size()=2
Result [Normal] is : 0.95331853628158569335937500000000
Result [Abnormal] is : 0.04668147489428520202636718750000

```
