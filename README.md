# param-siddhi-ai-gpu
PARAM Siddhi-AI is a high-performance computing-artificial intelligence (HPC-AI) and by far the fastest supercomputer developed in India with an Rpeak of 5.267 Pflops and 4.6 Pflops Rmax (Sustained)
has achieved **global ranking of 62*** in the TOP 500 most powerful supercomputer systems in the world, released on 16th November 2020

### how to use param siddhi ai-gpu for trainig  deep learninig  models



# installtion of cuda
-```cudnn```

-```half_cuda```

```opencv```


NOTE: Kindly use the versions provided to avoid any compilation issues.

## 1. Create a new conda environment.
  ```conda create --name myenv```

## 2. Install OpenCV.
  ```conda install -c anaconda libopencv=3.4.2```

## 3. Now, git clone alexeyab darknet repo.
  ```git clone https://github.com/AlexeyAB/darknet.git```

## 4.Install cmake(cmake 3.18 or higher is required).

```conda install -c anaconda cmake```

## 5. Setup CUDA to the desired version.
  ```source /opt/cuda-11.0.2/env.sh```

## 6. Install the supporting cuDNN.
  ```conda install cudnn=8.0 -c=conda-forge```


## 7. install CUDNN_HALF=1.
 ```cmake -DCMAKE_CUDA_ARCHITECTURES=75. ```

This will automatically set your CUDNN_HALF=1.

## 8. Run the cmake command inside darknet folder.
  ```cmake .```

##  9. Make sure no errors are present. Then run make command.
 ```make```

## 10. Run ./darknet to make sure it is working.
  ```Output:  usage: ./darknet <function>```


To check whether darknet is utilizing cuda,cudnn and opencv, download the following weights and run the given command.

1.``` wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights```

2.``` ./darknet detect cfg/yolov4.cfg yolov4.weights data/dog.jpg```
