# Amazing-AI-Painting

## Stable Diffusion2.0 Detailed Requirement
* **conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=11.3 -c pytorch**
* **pip install transformers==4.19.2 diffusers invisible-watermark**
* **pip install -e .**\
\
When installing PyTorch, it is essential to install the corresponding CUDA toolkit; otherwise, the *"Torch not compiled with CUDA enabled"* error will occur. If **torch.cuda.is_available()** returns **True**, then it is installed correctly.\
**other necessary packages**
* pip install omegaconf
* pip install einops
* pip install pytorch-lightning
* pip install open-clip-torch

#### xformers efficient attention
* export CUDA_HOME=/usr/local/cuda-11.3
* conda install -c nvidia/label/cuda-11.3.0 cuda-nvcc
* conda install -c conda-forge gcc
* conda install -c conda-forge gxx_linux-64==9.5.0




## Running
**text to image**
* **python scripts/txt2img.py --prompt "a professional photograph of an astronaut riding a horse" --ckpt pretrain/v2-1_768-ema-pruned.ckpt --config configs/stable-diffusion/v2-inference-v.yaml --H 768 --W 768 --device cuda --n_samples 1**
\
\
It's necessary to tune **n_sample** otherwise it's highly likely OOM.
\
\
**image to image**
* **python scripts/img2img.py --prompt "A fantasy landscape, trending on artstation" --init-img <path-to-img.jpg> --strength 0.8 --ckpt <path/to/model.ckpt>**
