# Yolov5 + Deep Sort with PyTorch





<div align="center">
<p>
<!––<img src="MOT16_eval/track_pedestrians.gif" width="400"/>
<!––<img src="MOT16_eval/track_all.gif" width="400"/>

</p>
<br>
<div>
<!-- <a href="https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch/actions"><img src="https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch/workflows/CI%20CPU%20testing/badge.svg" alt="CI CPU testing"></a>
<br>  
<a href="https://colab.research.google.com/drive/18nIqkBr68TkK8dHdarxTco6svHUJGggY?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> -->
 
</div>

</div>


## Introduction

This repository was edited from [this repo](https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch). I've added detect frontal faces for people who are looking at the camera and save result as `.csv` file. The detections generated by [YOLOv5](https://github.com/ultralytics/yolov5) and [dlib](https://pypi.org/project/dlib/), are passed to a [Deep Sort algorithm](https://github.com/ZQPei/deep_sort_pytorch) which tracks the objects. It can track any object that your Yolov5 model was trained to detect.


<!-- ## Tutorials

* [Yolov5 training on Custom Data (link to external repository)](https://github.com/ultralytics/yolov5/wiki/Train-Custom-Data)&nbsp;
* [Deep Sort deep descriptor training (link to external repository)](https://github.com/ZQPei/deep_sort_pytorch#training-the-re-id-model)&nbsp;
* [Yolov5 deep_sort pytorch evaluation](https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch/wiki/Evaluation)&nbsp; -->



## Before you run the tracker

<!-- 1. Clone the repository recursively:

`git clone --recurse-submodules https://github.com/duongcongnha/People-looking.git`

If you already cloned and forgot to use `--recurse-submodules` you can run `git submodule update --init`
 -->
1. Make sure that you fulfill all the requirements: Python 3.8 or later with all [requirements.txt](https://github.com/duongcongnha/ppattention-intermediary/blob/main/requirements.txt) dependencies installed, including torch>=1.7. To install, run:

`pip install -r requirements.txt`
<br></br>
    if you have problem with `pip install dlib`, try install `cmake` first
<br></br>
    if you have CUDA, delete two lines `torch>=1.7.0` and `torchvision>=0.8.1` in `requirements.txt` and install Pytorch with CUDA later.
    
## Config

`src/settings/config.yml`

## Cite

If you find this project useful in your research, please consider cite:

```latex
@misc{yolov5deepsort2020,
    title={Real-time multi-object tracker using YOLOv5 and deep sort},
    author={Mikel Broström},
    howpublished = {\url{https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch}},
    year={2020}
}
```
