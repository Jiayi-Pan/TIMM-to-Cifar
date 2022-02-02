# TIMM to Cifar100
General purpose script to (transfer) learn Cifar100 dataset for TIMM models

As it directly adopts the original training script of TIMM, the resulting performance should be extremely competitive compared to the casual made ones.

## Usage
- Intall dependencies
- Run script, below is an example of training efficientnet-b7 on cifar-100
  - Config ```model```, ```b```(batch size) as you wish :) 
```
python3 train.py \
/cifar-100-dataset \
--num-classes=100 \
-b=128 \
--img-size=224 \
--epochs=50 \
--color-jitter=0.4 \
--sched='cosine' \
--model-ema --model-ema-decay=0.995 --reprob=0.5 --smoothing=0.1 \
--pretrained \
--lr=2e-4 \
--model=tf_efficientnet_b7_ns \
--opt=adam \
--weight-decay=1e-4 \
--amp
```
