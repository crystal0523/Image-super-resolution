# Image-super-resolution

The purpose of this project is to implement a model for the task of instance segmentation using Tiny PASCAL VOC dataset. Detectron2 platform is used for this task. In particular, the model used is Mask R-CNN with ResNet50 as backbone. ImageNet pre-trained weights are used as a starting point for training.
The whole project is implemented using Google Colab platform.

## Environment

 ```
!pip install -U torch==1.5 torchvision==0.6 -f https://download.pytorch.org/whl/cu101/torch_stable.html
!pip install cython pyyaml==5.1
!pip install -U 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
!pip install detectron2==0.1.3 -f https://dl.fbaipublicfiles.com/detectron2/wheels/cu101/index.html
  ```
  
## Dataset
The dataset includes 291 training images and 14 test images.

------------------
<p align="center">
  <img src="25098.png">
</p>

<p align="center">
  <img src="26031.png">
</p>

-------------------


## Train

Using the following commands to start the training process. To see more detailed steps, refer to  ```instance_segmentation.ipynb ``` .
```
trainer = DefaultTrainer(cfg)
trainer.resume_or_load(resume=False)
trainer.train() 
```

## Results
------------------
image before scale 3

<img src="04.png">


image before scale 3
<img src="06.png">



-------------------

## Credits
1) https://github.com/2KangHo/vdsr_pytorch
2) https://github.com/twtygqyy/pytorch-vdsr
