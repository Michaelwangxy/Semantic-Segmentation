# Semantic-Segmentation



## Requirements of the Final Assignment

 Requirements: Implement its network architecture and basic training process under the PyTorch framework (the newer the model, the higher the basic score) , requiring the code to be implemented by yourself from scratch (if there is difficulty in the implementation, you can refer to the relevant code on github, but direct copying is not allowed. If found, it will be dealt with directly as zero points);
Report the metrics on the validation set on the Weizmann Horse dataset (https://www.kaggle.com/datasets/ztaihong/weizmann-horse-database/metadata) (the training validation set is randomly divided by the ratio of 0.85:0.15), metrics Including mIoU and Boundary IoU (Boundary IoU: Improving Object-Centric Image Segmentation Evaluation, CVPR'21) (reference indicator: the mIoU indicator reported by the model should be around 0.9 is normal);
Organize the assignment into a report submission, submit the relevant code to github, attach the link to the github repository in the report, and use MarkDown to write the code running instructions in ReadMe (refer to the format of https://github.com/poppinace/indexnet_matting) , the download link of the trained model should be attached, and the results of running the model should be consistent with the report.

## 

## Prepare Data
>Weizmann-Horse in Kaggle is available https://www.kaggle.com/datasets/ztaihong/weizmann-horse-database/metadata
>The dataset provides horses images and mask images. 
>the final path structure used in my code looks like this:

```dataset 
weizmann_horse_db
 ├──── horse 
 │ ├──── horse001.png 
 │ ├──── horse002.png 
 │ ├──── horse003.png
 │ ├──── ... 
 │ └──── horse327.png 
 ├──── mask 
 │ ├──── horse001.png 
 │ ├──── horse002.png 
 │ ├──── horse003.png
 │ ├──── ... 
 │ └──── horse327.png
 

```

## Explaination

Both models are written in jupyter notebook, and the visualization results of UNet and U2Net models are also saved in the corresponding .ipynb files .

The evaluation indicators of the model are determined by MIoU and BIoU, and the two models can still achieve good results when training a small number of rounds .

There is basically no computing power requirement for model training. Because the trained model is trained on the laptop.

You can use the [pretrained models](https://github.com/Michaelwangxy/Semantic-Segmentation/releases) to evaluate without training.(releases!)

## Citation

> [1] Ronneberger O, Fischer P, Brox T. U-net: Convolutional networks for biomedical image segmentation[C]//International Conference on Medical image computing and computer-assisted intervention. Springer, Cham, 2015: 234-241.
>
> [2] Qin X, Zhang Z, Huang C, et al. U2-Net: Going deeper with nested U-structure for salient object detection[J]. Pattern recognition, 2020, 106: 107404.
>
> [3] Cheng B, Girshick R, Dollár P, et al. Boundary IoU: Improving object-centric image segmentation evaluation[C]//Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2021: 15334-15342.

