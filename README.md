## Description
In this repository you will find Python wheels for the Raspberry Pi 4.
If you have a wish you can tell me as a pull request. At the moment it only has the latest version of Pytorch. I will always upload a wheel of the latest version in the future.
## Build Pytorch from the source
If you feel like you can build the wheel yourself with my step by step instructions.
But this is not necessary because I uploaded the latest wheel here.
 1. Run `sudo apt install libopenblas-dev libblas-dev m4 cmake cython python3-dev python3-yaml python3-setuptools`.
This command installs all dependencies of Pytorch.
 3. Change to the folder where you want to download Pytorch. (`cd PATH`)
 4. Run `git clone --recursive https://github.com/pytorch/pytorch`.
 5. Run `cd pytorch`.
 6. Run `export NO_CUDA=1`
`export NO_DISTRIBUTED=1`
`export NO_MKLDNN=1`
`export NO_NNPACK=1`
`export NO_QNNPACK=1`.
This command sets the environment variables.
 6. Run `python3 setup.py sdist bdist_wheel`.
This command takes a **few** hours.
 7. Look in the new subfolder "dist" for a file with the extension ".whl".
Copy the path and run `pip3 install PATH`.
 8. You can import Pytorch with `import torch`.
