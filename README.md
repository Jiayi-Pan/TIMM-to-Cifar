# TIMM to Cifar100
General purpose script to transfer learning Cifar100 dataset for TIMM models

As it directly adopts the original training script of TIMM, the resulting performance should be competitive than casual made ones.

## Usage
- Intall dependencies
- Run script, below is an example of training efficientnet-b0 on cifar-100
```
python3 train.py \
/cifar-100-dataset \
--num_classes=100
-b=128 \
--img-size=32 \
--epochs=50 \
--color-jitter=0 \
--sched='cosine' \
--model-ema --model-ema-decay=0.995 --reprob=0.5 --smoothing=0.1 \
--pretrained \
--lr=2e-4 \
--model=efficientnet_b0 \
--opt=adam \
--weight-decay=1e-4 \
```