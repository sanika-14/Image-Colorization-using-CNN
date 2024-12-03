# Image-Colorization-using-CNN
This project uses Convolutional Neural Networks (CNNs) to colorize grayscale images, based on approaches from ECCV16 and SIGGRAPH17. It predicts color channels and preserves textures and fine details for realistic results.
<!--<h3><b>Colorful Image Colorization</b></h3>-->


**+ automatic colorization functionality for Real-Time User-Guided Image Colorization with Learned Deep Priors, SIGGRAPH 2017!*


**Clone the repository; install dependencies**

```
git clone https://github.com/Image-Colorization-using-CNN
pip install requirements.txt
```

**Colorize!** This script will colorize an image. The results should match the images in the `imgs_out` folder.

```
python demo_release.py -i imgs/ansel_adams3.jpg
```

**Model loading in Python** The following loads pretrained colorizers. See [demo_release.py](demo_release.py) for some details on how to run the model. There are some pre and post-processing steps: convert to Lab space, resize to 256x256, colorize, and concatenate to the original full resolution, and convert to RGB.

```python
import colorizers
colorizer_eccv16 = colorizers.eccv16().eval()
colorizer_siggraph17 = colorizers.siggraph17().eval()
```
