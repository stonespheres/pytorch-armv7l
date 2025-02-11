# pytorch-armv7l
PyTorch 1.7.0 and torchvision 0.8.0 builds for RaspberryPi 4 (32bit OS)

### Dependencies

```bash
sudo apt install libopenblas-dev libblas-dev m4 cmake cython python3-dev python3-yaml python3-setuptools
```

### Build Options 
```bash
export NO_CUDA=1
export NO_DISTRIBUTED=1
export NO_MKLDNN=1 
export BUILD_TEST=0
export MAX_JOBS=4
```

### Compile
The wheel file will be created in `pytorch/dist/*` after running the following commands.
* PyTorch
```bash
git clone https://github.com/pytorch/pytorch --recursive && cd pytorch
git checkout v1.7.0
git submodule update --init --recursive
python setup.py bdist_wheel
```
* torchvision
```bash
git clone https://github.com/pytorch/vision && cd vision
git checkout v0.8.1
git submodule update --init --recursive
python setup.py bdist_wheel
```

### Reference

1. [Compling ARM stuff without an ARM board / Build PyTorch for the Raspberry Pi](https://nmilosev.svbtle.com/compling-arm-stuff-without-an-arm-board-build-pytorch-for-the-raspberry-pi)
2. [pytorch-arm-builds](https://github.com/nmilosev/pytorch-arm-builds)
3. [Python documentation](https://packaging.python.org/tutorials/managing-dependencies/)
