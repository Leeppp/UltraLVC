# UltraLVC: Decoder-Synchronized Progressive Entropy Modeling for Lossless Ultrasound Video Coding

## 1、dataset：
HMC-QU：https://www.kaggle.com/datasets/aysendegerli/hmcqu-dataset

SYS：https://drive.google.com/drive/folders/0B5LimsUgYY7ifjRfLUtxb1FRZ2ZXcHN0a0oyeFFUaXdyT2xBMDRpclZES0dTMS1uTXk3VjA?usp=sharing

CAMUS：https://www.creatis.insa-lyon.fr/Challenge/camus/

链接: https://pan.baidu.com/s/1FgIlCszQ0G0DjjgjnaZNZQ?pwd=bnad 提取码: bnad 

##  2、experiments



## 3、train and test

`python train_rec_BCM.py   --data_dir ./dataset  --dataset HMC-QU/ --crop_size 128 --hidden_unit 64 --lr 1e-4   --epochs 3000    --experiment_name HMC-QU-max  --weights model_HMC-QU-max.pth   --gpu_num 0   --decay_step 1000   --save_every 4    --print_every 1   --batch_size 16`

encode:
  `python encode_rec_BCM.py --gpu_num=0 --data_dir ./dataset  --dataset HMC-QU/ --crop_size 128 --hidden_unit 64 --lr 1e-4 --experiment_name HMC-QU-max   --weights model_HMC-QU-max.pth`

decode:
`python encode_rec_BCM.py --gpu_num=0 --data_dir ./dataset  --dataset HMC-QU/ --crop_size 128 --hidden_unit 64 --lr 1e-4 --experiment_name HMC-QU-max   --weights model_HMC-QU-max.pth`
