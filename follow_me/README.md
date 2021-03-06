# Semantic Segmentation - Follow Me

Jun Zhu

---

In this notebook, I built two segmentation networks to track VIP in an image. I used the data set for one of the projects at RoboND, Udacity. However, I have implemented different models. One is the original [SegNet](https://arxiv.org/pdf/1511.00561.pdf) and the other has a similar structure but all the convolutional layers are replaced by depthwise separable convolutional layers. Due to the technical constraint, **I have not combined the pooling indices in the encoder to the decoder!!!** Moreover, I used the default upsampling implemented in Keras which simply repeats the values in the lower layer and differs from bilinear upsampling.

## Requirements

- python3>=3.5.2
- tensorflow>=1.4.0
- keras>=2.0.9

## Run

```sh
python main.py --mode 0 --nn segnet  # train segnet
python main.py --mode 0 --nn depthwise-segnet  # train depthwise-segnet

python main.py --nn segnet  # infer all test images using trained segnet
python main.py --nn depthwise-segnet  # infer all test images using traind depthwise-segnet
```

## Visualization

```sh
$ jupyter notebook follow_me.ipynb
```
