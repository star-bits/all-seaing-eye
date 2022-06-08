# All-SEAing Eye (Proof of Concept)

![All-SEAing Eye](https://user-images.githubusercontent.com/93939472/170851486-ef6c8707-0ab0-414e-83f2-74de666aba57.png)

## Install mmdetection

Install mmdetection using [mmdet_install.ipynb](https://github.com/star-bits/all-seaing-eye/blob/main/mmdet_install.ipynb).

## Download dataset

Download dataset from [AI Hub 해상 객체 이미지](https://aihub.or.kr/aidata/34155)

## Rename image files and Generate annotation files

Organize the dataset directory as follows:
```
./mmdetection/data/
    test/
        images/
            20201112/
            ...
    train/
        images/
            20201216/
            ...
        labels/
            20201216/
            ...
    valid/
        images/
            20201224/
            ...
        labels/
            20201224/
            ...
```
Put [anns_generate_files_rename.ipynb](https://github.com/star-bits/all-seaing-eye/blob/main/anns_generate_files_rename.ipynb) inside `mmdetection/data` and run it. It'll rename filenames from Korean to English (which is vital for mmdetection model to process images), and create annotation files `test.json`, `train.json`, and `valid.json` in COCO format. 

## Train and Inference

Place [swin_faster_cfg.py](https://github.com/star-bits/all-seaing-eye/blob/main/swin_faster_cfg.py), [test.ipynb](https://github.com/star-bits/all-seaing-eye/blob/main/test.ipynb), and [train.ipynb](https://github.com/star-bits/all-seaing-eye/blob/main/train.ipynb) in `mmdetection/tools` and run `train.ipynb` to train, and `test.ipynb` to get inference. 

Faster R-CNN with Swin-Tiny backbone is used. 

### Ground truth visualized:
![gt](https://github.com/star-bits/all-seaing-eye/blob/main/images/gt.png)

### Inference result visualized:

![output-1](https://github.com/star-bits/all-seaing-eye/blob/main/images/output-1.png)
![output-2](https://github.com/star-bits/all-seaing-eye/blob/main/images/output-2.png)
![output-3](https://github.com/star-bits/all-seaing-eye/blob/main/images/output-3.png)
![output-4](https://github.com/star-bits/all-seaing-eye/blob/main/images/output-4.png)
![output-5](https://github.com/star-bits/all-seaing-eye/blob/main/images/output-5.png)
