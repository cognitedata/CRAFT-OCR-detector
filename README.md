# OCR detector for PNID based on CRAFT: CRAFT: Character-Region Awareness For Text detection
This is an adaptation of the official Pytorch implementation of CRAFT text detector | [Paper](https://arxiv.org/abs/1904.01941) by

**[Youngmin Baek](mailto:youngmin.baek@navercorp.com), Bado Lee, Dongyoon Han, Sangdoo Yun, Hwalsuk Lee.**
Clova AI Research, NAVER Corp.

## Sample Results
TODO

### Overview
PyTorch implementation for CRAFT text detector that effectively detect text area by exploring each character region and affinity between characters. The bounding box of texts are obtained by simply finding minimum bounding rectangles on binary map after thresholding character region and affinity scores. 

<img width="1000" alt="teaser" src="./figures/craft_example.gif">

## Getting started
### Install dependencies
The following are required packages:
- PyTorch>=0.4.1
- torchvision>=0.2.1
- opencv-python>=3.4.2
Also check requirements.txt for additional required packages:
```
pip install -r requirements.txt
```

## Training
TODO 
Training code is not included yet
It is planned to bootstrap the training using synthetic data from Synthtext | [Repo](https://github.com/ankush-me/SynthText)


## Testing
TODO

The result image and score maps will be saved to `./result` by default.

### Arguments
* `--trained_model`: pretrained model
* `--text_threshold`: text confidence threshold
* `--low_text`: text low-bound score
* `--link_threshold`: link confidence threshold
* `--cuda`: use cuda for inference (default:True)
* `--canvas_size`: max image size for inference
* `--mag_ratio`: image magnification ratio
* `--poly`: enable polygon type result
* `--show_time`: show processing time
* `--test_folder`: folder path to input images
* `--refine`: use link refiner for sentense-level dataset
* `--refiner_model`: pretrained refiner model


## Links
- Repo of recognition : https://github.com/clovaai/deep-text-recognition-benchmark

## License
```
Copyright (c) 2019-present NAVER Corp.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
