
<div align="left">

# <div align="center">LDMS-UAV: Small Object Detection in UAV Images Based on Multiscale Features and Lightweight Decoupling</div>

This is the code for the method proposed in the paper. We provide the weight files for the experimental effects in the paper, as well as the specific code implementation of each module.
The model can be trained or tested after installing the runtime environment.

## <div align="left">Quick Start Examples</div>

<details open>
<summary>Install</summary>

First, clone the project and configure the environment.
[**Python>=3.7.0**](https://www.python.org/), [**PyTorch>=1.7**](https://pytorch.org/get-started/locally/).

```bash
git clone https://github.com/toscen/LDMS-UAV  # clone
cd LDMS-UAV
pip install -r requirements.txt  # install
```
</details>

<details open>
<summary>Train</summary>

We perform experiments on the YOLOv7-tiny network and use official pre-training weights. The VisDrone dataset is used for training and testing.
Then start the training with the following command:

```python
python train.py --weights yolov7-tiny.pt --cfg cfg/training/yolov7-tiny-3ideamsc2f-Simelan.yaml --data data/mydata.yaml
```
</details>


<details>
<summary>Test</summary>

We provide the weight file described in the paper, which can be used with commands to reproduce the model effects:

```bash
python test.py --data data/mydata.yaml --weights best.pt --task test
```
</details>

## <div align="left"> VisDrone dataset</div>
The dataset is the same as the official website.
