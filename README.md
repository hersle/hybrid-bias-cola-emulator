# Hybrid bias COLA emulator

## Installation

```sh
git clone --recursive https://github.com/hersle/hybrid-bias-cola-emulator
make -C hi_class_public/ class # compile CLASS (possibly needs -std=gnu17)
make -C FML/FML/COLASolver/ nbody # compile COLA

# With Conda environment.toml
conda env create -f environment.yml
conda env update --file environment.yml --prune
conda activate hybrid-bias-cola-emulator
# etc.

# With Python pyproject.toml
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

## Notes

- Other hiclass versions than the one included in this project's git submodule may crash with Brans-Dicke.
