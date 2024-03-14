# OKGR: Occluded Keypoint Generation and Refinement for 3D Object Detection (PRCV 2023)
 This code is based on [MindSpore](https://gitee.com/mindspore/mindspore).

## Install
a. Install the [MindSpore(CPU)](https://www.mindspore.cn/install): 

If your machine is Linux-x86_64 and you have Python 3.7, you can run the following command:

```shell
pip install https://ms-release.obs.cn-north-4.myhuaweicloud.com/2.2.11/MindSpore/unified/x86_64/mindspore-2.2.11-cp37-cp37m-linux_x86_64.whl --trusted-host ms-release.obs.cn-north-4.myhuaweicloud.com -i https://pypi.tuna.tsinghua.edu.cn/simple
```

b. Install the dependent libraries as follows: 

Install the SparseConv library, we use the implementation from [Spconv](https://github.com/traveller59/spconv).

Install the dependent python libraries: 

```shell
pip install -r requirements.txt
```

c. Install this pcdet library and its dependent libraries by running the following command:
```shell
python setup.py develop
```

## Data Preparation
Please follow the instructions in [OpenPCDet](https://github.com/open-mmlab/OpenPCDet).

## Testing
You could optionally add extra command line parameters `--batch_size ${BATCH_SIZE}`, `${NUM_GPUS}` to specify your preferred parameters.

If you want to test, you need to download the trained [model file](https://pan.baidu.com/s/1YIbqiRA_jnSwPc6GbmBMKg)[9n3i].
* Test :
```shell
python test.py --cfg_file ./tools/cfgs/kitti_models/pv_rcnn_pp.yaml --batch_size ${BATCH_SIZE} --ckpt ${CKPT}
```
## Reference
If you use OKGR in your research, please cite our work by using the following BibTeX entry:
```shell
@inproceedings{ji2023okgr,
  title={OKGR: Occluded Keypoint Generation and Refinement for 3D Object Detection},
  author={Ji, Mingqian and Yang, Jian and Zhang, Shanshan},
  booktitle={Chinese Conference on Pattern Recognition and Computer Vision (PRCV)},
  pages={3--15},
  year={2023},
  organization={Springer}
}
```
