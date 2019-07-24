# Test code for BONN
## Prepare
* install the latest PyTorch (1.1.0)
* download this code (pretrained model included)
* get the ImageNet validation set ready (you may need the script *valprep.sh* to pre-process the val set)

## Check whether the weights and activation is binary
* run ```python weight_summary.py``` to check whether the weights are binary
* check the code in the module ```BinConv2d``` to see whether the input for convolution is binary

## Evaluation 
Modifications in the script ```evaluate_imagenet.sh```:
* modify the **PATH to your ImageNet dataset** 
* modify the **batchsize** (default: 256) according to your hardware (at least one GPU is requried)

Run the script ```evaluate_imagenet.sh``` and the accuracy on validation set is around **59.40**. 

## Please cite

```
@inproceedings{gu2019bonn,
  title={Bayesian Optimized 1-bit CNNs},
  author={Gu, Jiaxin and Zhao, Junhe and Jiang, Xiaolong and Zhang, Baochang and Liu Jianzhuang and Guo, Guodong and Ji, Rongrong},
  booktitle={Proceedings of the IEEE International Conference on Computer Vision},
  year={2019}
}
```

