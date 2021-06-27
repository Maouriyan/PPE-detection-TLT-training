# PPE-detection-TLT-training

## Steps to perform PPE Detection:

- Install dependencies and Docker Container <br/>
  - On Training Machine with NVIDIA GPU:
      - Install NVIDIA Docker Container: [installation instructions](https://developer.nvidia.com/blog/gpu-containers-runtime/) [TLT Toolkit Requirements](https://docs.nvidia.com/metropolis/TLT/tlt-getting-started-guide/index.html#requirements) <br/>
      - [Running Transfer Learning Toolkit using Docker](https://ngc.nvidia.com/catalog/containers/nvidia:tlt-streamanalytics)
          - Pull docker container:<br/>
              ```docker pull nvcr.io/nvidia/tlt-streamanalytics:v2.0_py3```
          - Run the docker image:
              ```
              docker run --gpus all -it -v "/path/to/dir/on/host":"/path/to/dir/in/docker" \
                            -p 8888:8888 nvcr.io/nvidia/tlt-streamanalytics:v2.0_py3 /bin/bash
              ```
      - Clone Git repo in TLT container:
          ```
          git clone https://github.com/Maouriyan/PPE-detection-TLT-training.git
          ```
       - Run Jupter Notebook in TLT container:
          ```
          jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
          ```
       - Open helmet-detection.ipynb and follow the steps to create engine file.
       - To run the application , update your model in /models in https://github.com/Maouriyan/PPE-detection-deepstream


###Citations 

https://github.com/NVIDIA-AI-IOT/face-mask-detection
https://github.com/AnshulSood11/PPE-Detection-YOLO-Deep_SORT

          
          
