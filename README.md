# Amazing-AI-Painting

## Stable Diffusion2.0 Detailed Requirement
* **conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=11.3 -c pytorch**
* **pip install transformers==4.19.2 diffusers invisible-watermark**
* **pip install -e .**\
When installing PyTorch, it is essential to install the corresponding CUDA toolkit; otherwise, the *"Torch not compiled with CUDA enabled"* error will occur. If **torch.cuda.is_available()** returns **True**, then it is installed correctly.
