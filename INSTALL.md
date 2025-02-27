# Installation

This repository is built in PyTorch 1.11 and tested on Ubuntu 16.04 environment (Python3.7, CUDA10.2, cuDNN7.6).
Follow these intructions

1. Clone our repository
```
git clone https://github.com/swz30/MIRNetv2.git
cd MIRNetv2
```

2. Make conda environment
```
conda create -n pytorch111 python=3.7
conda activate pytorch111
```

3. Install dependencies
```
# conda install pytorch=1.11 torchvision cudatoolkit=10.2 -c pytorch
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113
pip install matplotlib scikit-learn scikit-image opencv-python yacs joblib natsort h5py tqdm
pip install einops gdown addict future lmdb numpy pyyaml requests scipy tb-nightly yapf lpips Cython
```

4. Install basicsr
```
python setup.py develop --no_cuda_ext
```

### Download datasets from Google Drive

To be able to download datasets automatically you would need `go` and `gdrive` installed. 

1. You can install `go` with the following
```
curl -O https://storage.googleapis.com/golang/go1.11.1.linux-amd64.tar.gz
mkdir -p ~/installed
tar -C ~/installed -xzf go1.11.1.linux-amd64.tar.gz
mkdir -p ~/go
```

2. Add the lines in `~/.bashrc`
```
export GOPATH=$HOME/go
export PATH=$PATH:$HOME/go/bin:$HOME/installed/go/bin
```

3. Install `gdrive` using
```
go get github.com/prasmussen/gdrive
```

4. Close current terminal and open a new terminal. 
