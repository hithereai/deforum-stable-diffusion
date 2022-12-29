
# Deforum Stable Diffusion

<p align="left">
    <a href="https://github.com/deforum-art/deforum-stable-diffusion/commits"><img alt="Last Commit" src="https://img.shields.io/github/last-commit/deforum-art/deforum-stable-diffusion"></a>
    <a href="https://github.com/deforum-art/deforum-stable-diffusion/issues"><img alt="GitHub issues" src="https://img.shields.io/github/issues/deforum-art/deforum-stable-diffusion"></a>
    <a href="https://github.com/deforum-art/deforum-stable-diffusion/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/deforum-art/deforum-stable-diffusion"></a>
    <a href="https://github.com/deforum-art/deforum-stable-diffusion/network"><img alt="GitHub forks" src="https://img.shields.io/github/forks/deforum-art/deforum-stable-diffusion"></a>
    <a href="https://colab.research.google.com/github/deforum-art/deforum-stable-diffusion/blob/main/Deforum_Stable_Diffusion.ipynb"><img alt="Colab" src="https://colab.research.google.com/assets/colab-badge.svg"></a>  
</p>

### Before you start
- Create a [huggingface](https://huggingface.co/settings/tokens) account, to get the token which you will need for auto model download.
- Install [ffmpeg](https://ffmpeg.org/download.html), and make sure it's in your PATH by running ```bash ffmpeg -h``` in your Windows CMD/ Linux Terminal. If you don't get an error you're good. 
- Install [anaconda](https://www.anaconda.com/) for managing python environments and packages
- Install git for your system if you don't already have it installed. Easiest way is to open an Anaconda Prompt (CLI) and type:
```
conda install -c anaconda git -y
```
If you are having problems with installng git via Anaconda, please use the following links instead:

[git for Windows](https://git-scm.com/download/win)

[git for Linux](https://git-scm.com/download/linux)

### Getting Started
1. Open anaconda Prompt-CLI (on Windows) or terminal (on Linux) and navigate to your desired installation folder
2. Clone the github repository and navigate to it:
```
git clone https://github.com/deforum-art/deforum-stable-diffusion.git
cd deforum-stable-diffusion

```
3. create a suitable anaconda environmentfor Deforum, activate it, and install Pytorch:
```
conda create -n deforum python=3.10.6
conda activate deforum
pip3 install torch==1.12.1+cu113 torchvision==0.13.1+cu113 --extra-index-url https://download.pytorch.org/whl/cu113
```
4. install required packages:
```
python -m pip install -r requirements.txt
```
5. check your installation by running the .py:
```
python Deforum_Stable_Diffusion.py
```
You have successfully installed deforum stable diffusion if the python file runs without any errors.

## Starting Over
The stable-diffusion folder can be deleted and the dsd conda environment can be removed with the following set of commands:
```
conda deactivate
conda env remove -n deforum

```
With the deforum environment removed you can start over.


## Running Deforum Stable Diffusion
There are four ways to run deforum stable diffusion:
- Locally through colab Local runtime
- Online using colab servers and GPUs. 
- Locally with the .py file (not recommended)
- Locally with jupyter (not recommended)

### Running Locally
make sure the deforum conda environment is active:
```
conda activate dsd
```
navigate to the stable-diffusion folder and run either the Deforum_Stable_Diffusion.py or the Deforum_Stable_Diffusion.ipynb. running the .py is the quickest and easiest way to check that your installation is working, however, it is not the best environment for tinkering with prompts and settings
```
python Deforum_Stable_Diffusion.py

```
if you prefer a more colab-like experience you can run the .ipynb in jupyter-lab or jupyter-notebook. activate jupyter-lab or jupyter-notebook from within the stable-diffusion folder with either of the following commands:
```
jupyter-lab

```
```
jupyter notebook

```


### Colab Local Runtime
make sure the dsd conda environment is active:
```
conda activate dsd

```
open google colab. file > upload notebook > select .ipynb file in the stable-diffusion folder. enable jupyter extension. note: you only need to run this cell one time
```
jupyter serverextension enable --py jupyter_http_over_ws

```
start server
```
jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8888 --NotebookApp.port_retries=0
  
```
copy paste url token


### Colab Hosted Runtime
Deforum_Stable_Diffusion.ipynb can be uploaded to colab and run normally in a hosted session
