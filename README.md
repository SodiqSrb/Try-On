# Try-On
 Given a profile image and a source image containing cloth, it applies the cloth to your profile image and let you see how does it look on you as if you were actually wearing it.

# Features

<img src="https://github.com/xanjay/cmate-virtual-tryon/blob/master/src/flask_app/static/images/logo.png" height="200" /><br>
<img src="https://img.shields.io/docker/cloud/build/xanjay/cmate" /><br>
## About This Project
SRB is a virtual clothing try on tool. Given a profile image and a source image containing cloth, it applies the cloth to your profile image and let you see how does it look on you as if you were actually wearing it.<br>
It is a flask web application powered by deep learning and GAN. 
<img src="https://github.com/xanjay/cmate-virtual-tryon/blob/master/docs/cmate-demo.gif" height="300" /><br>
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



## References
- Deeplab: https://github.com/tensorflow/models/tree/master/research/deeplab
- Deepfashion2 Dataset: https://github.com/switchablenorms/DeepFashion2
- Openpose: https://github.com/CMU-Perceptual-Computing-Lab/openpose


