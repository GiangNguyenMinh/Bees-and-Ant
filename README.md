![Been And Ant](https://st2.depositphotos.com/7413918/10253/i/950/depositphotos_102537306-stock-photo-ant-and-bee-with-white.jpg)
# Object detect Bee and Ant

## Install 
```bash
$ git clone https://github.com/ultralytics/yolov5.git
$ cd yolov5
$ git install -r requirements.text
```
## Download dataset

Download directly in [here](https://app.roboflow.com/giang113404-gmail-com/beeandant/1)
or paste this snippet into a notebook:
```bash
!pip install roboflow

from roboflow import Roboflow
rf = Roboflow(api_key="dF790Y9GvhJvFReq4jzf")
project = rf.workspace().project("beeandant")
dataset = project.version(1).download("yolov5")
```

## Inference
```bash
$ python detect.py --weights /Bees-and-Ant/run/exp/beeandant 
                   --source /Bees-and-Ant/data/test/images 
                   --name detect_result
```
## Training
#### Run with full option 
```
$ python train.py --weights yolov5s.pt --cfg models/yolov5s.yaml 
                  --data data/custom_data.yaml --epochs 100 
                  --batch-size 64 --imgsz 640 --workers 16 --name beeandant           
```
#### Select option
```bash
$ python train.py --weights yolov5s.pt --cfg models/yolov5s.yaml --data data/custom_data.yaml --epochs 100
                          yolov5m.pt              yolov5m.yaml
                          yolov5l.pt              yolov5l.yaml
                          yolov5n.pt              yolov5n.yaml
                          yolov5x.pt              yolov5x.yaml
```
#### Train colab 
Colab code [click here](https://colab.research.google.com/drive/15f4IXID5VAeAmS5Id9ncXBc1F6w44F_A#scrollTo=zKKqh9sdxe7d)




