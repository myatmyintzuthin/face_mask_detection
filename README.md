# face_mask_detection

[![TensorFlow 2.6](https://img.shields.io/badge/TensorFlow-2.6-FF6F00?logo=tensorflow)](https://github.com/tensorflow/tensorflow/releases/tag/v2.6.0) 



![webcam_test](https://github.com/myatmyintzuthin/face_mask_detection/blob/main/assets/webcam_test.gif)
------
#### Dataset
The [Face mask Dataset](https://github.com/myatmyintzuthin/face_mask_detection/releases/download/v1.0.0/face_mask_dataset.zip) is collected and annotated by Self-Study-Camp team members on 22 November 2021. The dataset consists of 208 images splitted into 168 train, 40 test images in XML format.

![dataset.PNG](https://github.com/myatmyintzuthin/face_mask_detection/blob/main/assets/dataset.PNG)
------
#### Model 
We will be using SSD-mobilenetv2 model from [TensorFlow 2 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md). They provide a collection of detection models pre-trained on the [COCO 2017 dataset](https://cocodataset.org/).
| Model name  | Speed (ms)  | COCO mAP | Outputs |
| ----------- | ----------- | -------- | ------- |
| [SSD MobileNet V2 FPNLite 640x640](http://download.tensorflow.org/models/object_detection/tf2/20200711/ssd_mobilenet_v2_fpnlite_640x640_coco17_tpu-8.tar.gz)      | 39      | 28.2 | Boxes |
------
#### Metrics
After training for 8000 steps:
```
{'Loss/classification_loss': 0.06144937,
 'Loss/localization_loss': 0.017765515,
 'Loss/regularization_loss': 0.12342198,
 'Loss/total_loss': 0.20263687,
 'learning_rate': 0.07603875}
```
Validation Detection Metrics:

```
Accumulating evaluation results...
DONE (t=0.06s).
 Average Precision  (AP) @[ IoU=0.50:0.95 | area=   all | maxDets=100 ] = 0.343
 Average Precision  (AP) @[ IoU=0.50      | area=   all | maxDets=100 ] = 0.698
 Average Precision  (AP) @[ IoU=0.75      | area=   all | maxDets=100 ] = 0.399
 Average Precision  (AP) @[ IoU=0.50:0.95 | area= small | maxDets=100 ] = 0.700
 Average Precision  (AP) @[ IoU=0.50:0.95 | area=medium | maxDets=100 ] = 0.515
 Average Precision  (AP) @[ IoU=0.50:0.95 | area= large | maxDets=100 ] = 0.313
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets=  1 ] = 0.348
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets= 10 ] = 0.449
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets=100 ] = 0.552
 Average Recall     (AR) @[ IoU=0.50:0.95 | area= small | maxDets=100 ] = 0.700
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=medium | maxDets=100 ] = 0.693
 Average Recall     (AR) @[ IoU=0.50:0.95 | area= large | maxDets=100 ] = 0.511
```
#### Tensor Board Metrics
![tensorboard.png](https://github.com/myatmyintzuthin/face_mask_detection/blob/main/assets/tensorboard.png)
------
#### References
[TensorFlow Object Detection API Tutorial](https://readthedocs.org/projects/tensorflow-object-detection-api-tutorial/) \
[TensorFlow 2 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md)

 





