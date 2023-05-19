# Try-On
 Given a profile image and a source image containing cloth, it applies the cloth to your profile image and let you see how does it look on you as if you were actually wearing it.
 
## About This Project
This intending project is a virtual clothing try on tool. Given a profile image and a source image containing cloth, it applies the cloth to your profile image and let you see how does it look on you as if you were actually wearing it.<br>
It will be a flask web application powered by deep learning and GAN. 

### Features
- Supports all kinds of upper wear clothes for both men and women.
- Accurate cloth extraction and fitting.
- Simple, elegent and easy to use web app.

### How does it work ?
It works by extractng cloth from source image and fitting into your profile image.<br>
Under the hood, it uses two separate deep learning models:<br>
**Cloth segmentation model**: Custom Deeplab model to extract cloth from source image.<br>
**Pose estimator model**: Pretrained Openpose body_25 model used to locate shoulder points.<br>
Extracted cloth is blended into profile image based on shoulder location.

## Dataset
- **Deepfashion2 Dataset**: used to train cloth segmentation model.
- **MultiGarmentNetwork**
- DeepFashion2 is a comprehensive fashion dataset. It contains 491K diverse images of 13 popular clothing categories from both commercial shopping stores and consumers. It totally has 801K clothing clothing items, where each item in an image is labeled with scale, occlusion, zoom-in, viewpoint, category, style, bounding box, dense landmarks and per-pixel mask.There are also 873K Commercial-Consumer clothes pairs.
The dataset is split into a training set (391K images), a validation set (34k images), and a test set (67k images).

- Multi-Garment Network (MGN), a method to predict body shape and clothing, layered on top of the SMPL model from a few frames (1-8) of a video. Several experiments demonstrate that this representation allows higher level of control when compared to single mesh or voxel representations of shape. Our model allows to predict garment geometry, relate it to the body shape, and transfer it to new body shapes and poses. To train MGN, we leverage a digital wardrobe containing 712 digital garments in correspondence, obtained with a novel method to register a set of clothing templates to a dataset of real 3D scans of people in different clothing and poses. Garments from the digital wardrobe, or predicted by MGN, can be used to dress any body shape in arbitrary poses.


## General info
This project is a part of my research project in juxtaposition with my freelancing work https://www.fiverr.com/s/1QZ9qp. While buying clothes online, it is difficult for a customer to select a desirable outfit in the first attempt because they can’t try on clothes. This project aims to solve this problem.

<img width="383" alt="general_info" src="https://user-images.githubusercontent.com/63489382/163923011-c2898812-2491-4ec2-beb7-dcaaaf680e4f.png">


## Demo

https://user-images.githubusercontent.com/63489382/163922795-5dbb0f52-95e4-42c6-95d7-2d965abeba6d.mp4



## Block Diagram
![block_diagram_whole](https://user-images.githubusercontent.com/63489382/163922947-c1677f79-ad6f-4550-affc-7d4e80f0d247.png)


## Methodology
![block_diagram_detailed](https://user-images.githubusercontent.com/63489382/163922991-86d148c2-1a97-48a5-b4ec-d8c16819374a.png)




## Citation
**Work in progress**


## References
- Deeplab: https://github.com/tensorflow/models/tree/master/research/deeplab
- Deepfashion2 Dataset: https://github.com/switchablenorms/DeepFashion2
- Openpose: https://github.com/CMU-Perceptual-Computing-Lab/openpose


