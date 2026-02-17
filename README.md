# Hybrid bias COLA emulator

## Installation

```sh
git clone --recursive https://github.com/hersle/hybrid-bias-cola-emulator
make -C hi_class_public/ class # compile CLASS
make -C FML/FML/COLASolver/ nbody # compile COLA
conda deactivate # optional
python -m venv venv # optional
source venv/bin/activate
pip install -e .
ipython kernel install --user --name=venv --display-name="hybrid-bias-cola-emulator (local environment)"
```

## Usage

```sh
jupyter-lab --no-browser # on server
ssh -L 9999:localhost:8888 your-cluster-machine # on client
```
