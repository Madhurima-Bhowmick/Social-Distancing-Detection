# Social-Distancing-Detection

This is the final year major project based on Machine Learning, developed as instructed by our college.

It is a Deep Learning based model for Social Distance Detection using YOLOv3 algorithm and trained on COCO dataset. This tool has a mail alert system which sends alerts to the registered mail address if social distance violation is caused. The model was developed to help in tackling COVID-19.

### Libraries to be installed

1. OpenCV
2. Numpy
3. Scipy
4. Argparse
5. Pandas
6. Imutils


### Theory

A real-time model, it uses webcam or IP camera for object detection from an overhead view and determines the bounding box information. 

Using the Euclidean Distance, the pairwise centroid distances between detected bounding boxes are measured.

A threshold is defined to check social distance violation among people, here it is set as 80 pixels. If the centroid distance between two bounding box is less than 80 pixel, then it sets the box color as red as a trigger to social distance violation. Yellow color is set if pedestrians are on the verge of violation, and grenn bounding box refers that centroid distance is far greater than 80 pixel representing safe distance.

As a person's appearance vary significantly from an overhead view, transfer learning method is used to improve the pre-trained model's performance.


### To run the model

In mylib/config.py

```set url = 0 for using webcam```

```set url = '' as IP camera url```

```set alert = true for mail alerts```

To run the program in real-time

```python run.py```
