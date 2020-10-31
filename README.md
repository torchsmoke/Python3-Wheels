## Description
In this repository you will find Python wheels for the Raspberry Pi 4.
If you have a wish you can tell me as a issue. I will always upload a wheel of the latest version in the future.
I couldn't upload the whole wheels so it is divided into sub-archives.
## Build Pytorch from the source
If you feel like you can build the wheel yourself with my step by step instructions.
But this is not necessary because I uploaded the latest wheel here.
 1. Run `sudo apt install libopenblas-dev libblas-dev m4 cmake cython python3-dev python3-yaml python3-setuptools`.
This command installs all dependencies of Pytorch.
 3. Change to the folder where you want to download Pytorch. (`cd PATH`)
 4. Run `git clone --recursive https://github.com/pytorch/pytorch`.
 6. Run `cd pytorch`.
 7. Run `export NO_CUDA=1`
`export NO_DISTRIBUTED=1`
`export NO_MKLDNN=1`
`export NO_NNPACK=1`
`export NO_QNNPACK=1`.
This command sets the environment variables.
 8. Run `python3 setup.py sdist bdist_wheel`.
This command takes a **few** hours. (On Raspberry Pi 4 4GB with 2294MHz it take round 3 hours)
 9. Look in the new subfolder "dist" for a file with the extension ".whl".
Copy the path and run `pip3 install PATH`.
 10. You can import Pytorch with `import torch`.
 
 ## Install the wheel
If you want to install the wheel, download the files.
If the file extension .whl you can install it normal.
Otherwise follow the instructions below.
It is easiest if you have installed the file-roller package.
Double-click on the file with the extension .001.
Extract the only .whl file.
Copy the path of the extracted file and enter `sudo pip3 install [path]` in the terminal and press Enter.
Now it should be installed.
