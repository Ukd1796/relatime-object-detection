Object detection using realtime videos 
comparing yolo-v8 and faster r-cnn

Link:
Real-world Image Datasets For Federated Learning
https://arxiv.org/pdf/1910.11089.pdf


Dataset Used:
The dataset used in this project is KITTI Dataset, a real-world computer vision benchmark designed specifically for autonomous driving.
The dataset consists of 7481 training images and 7518 test images. It consists of 8 classes: Car, Van, Truck, Pedestrian, Person sitting, Cyclist, Tram, and Misc. Some of the object whic were not close to the scanner are classified as DontCare

Implementation:

Implemented Object detection using YOLO framework in TensorFlow
The Federated Learning set up incorporates a client-server model
We have implemented weights aggregation using Federated Averaging Algorithm
We are using connection-oriented TCP protocol to establish communication between the server and the clients. This protocol is implemented using Socket library available in Python.
The weights file and client metadata are encrypted in the client node before transferring them via socket to the server. The server decrypts the files, performs secure aggregation of the weights, and encrypts them back before re sending to the client. We have implemented this using Python package called cryptography.