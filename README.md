# Kaggle
A repository to get help me dive into AI/ML!

## Getting started if using a remote machine
Make a conda environment in Python 3.6
```
conda create -n kaggle python=3.6
```

Then activate it and install the necessary dependicies as follows
```
conda activate kaggle
pip3 install -r requirements.txt
```

## Jetson Nano Headless Setup
Because TensorFlow more optimized for NVIDIA GPUs with CUDA core support, this is my headless remote setup for training with GPUs!

```
ssh jetsonpark@192.168.1.124
cd <directory where code lives>
jupyter notebook --no-browser --port=9000
```

Note that port number doesn't matter, just make sure it's an unused port! After that is settled, make a new terminal window and forward your remote port to your local one! I used the same port for convenience, but again make sure it's an unused port on your local machine!

```
ssh -N -f -L localhost:9000:localhost:9000 jetsonpark@192.168.1.124
```
