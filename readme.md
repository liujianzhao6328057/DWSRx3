## Deep wavelet prediction for image super-resolution
The testing code for [_Deep wavelet prediction for image super-resolution, CVPRW, 2017_](http://openaccess.thecvf.com/content_cvpr_2017_workshops/w12/html/Guo_Deep_Wavelet_Prediction_CVPR_2017_paper.html), NTIRE 2017 Super-Resolution Challenge - DWSRx3.

### Other scale: [DWSRx2](https://github.com/tT0NG/WvSRx2);  [DWSRx4](https://github.com/tT0NG/DWSRx4)

### Pre-requirement
Python package requirement:

- tensorflow w/GPU @ https://github.com/tensorflow/tensorflow
- pywt @ https://github.com/PyWavelets/pywt
- cv2  @ https://github.com/opencv/opencv

### To execute: 
1. In terminal, type in `python DWSRx3.py`
2. Then a promote asks for testing data set: `Please enter the testing path [hit enter to run default set]:` 
3. Hit enter to run default testing set from DIV2K NTIRE which is stored at: `./Testx3Lum`
4. The final results will be stored at: `./Resultx3Lum`
5. Run `FinalColorSRx3.m` to generate final color SR and store the results in `./Resultx3Color`

### NOTE:
1. The testing data should be bicubic enlarged version of the original down-sampled version. For example, to generate `x3` super-resolution results, the original `x3` down-sampled low-resolution image should first be enlarged to `x3` size, then fed the enlarged version to DWSR (as described in the fact sheet). Use `generateTestX3.m` to generate enlarged LR luminance image.
2. The DWSR weights are stored at: `./Weightx3`
3. The DWSR model is defined in: `netx3.py`
4. The script is *NOT* for training.


_The training code is not fully cleaned up; for academic purpose, please request training from [here](https://docs.google.com/forms/d/e/1FAIpQLScYcA_MZ2J5SWIdjxxDEEVJZ9nKAio9Yu2iIdSlxTBXDDe0MA/viewform) by providing basic usage information._

### Cite us
```
@inproceedings{guo2017deep,
  title={Deep wavelet prediction for image super-resolution},
  author={Guo, Tiantong and Mousavi, Hojjat Seyed and Vu, Tiep Huu and Monga, Vishal},
  booktitle={The IEEE Conference on Computer Vision and Pattern Recognition (CVPR) Workshops},
  year={2017}
}
```
```
@inproceedings{timofte2017ntire,
  title={Ntire 2017 challenge on single image super-resolution: Methods and results},
  author={Timofte, Radu and Agustsson, Eirikur and Van Gool, Luc and Yang, Ming-Hsuan and Zhang, Lei and Lim, Bee and Son, Sanghyun and Kim, Heewon and Nah, Seungjun and Lee, Kyoung Mu and others},
  booktitle={Computer Vision and Pattern Recognition Workshops (CVPRW), 2017 IEEE Conference on},
  pages={1110--1121},
  year={2017},
  organization={IEEE}
}
```
____________
Tiantong@iPAL2017, tong.renly@gmail.com
