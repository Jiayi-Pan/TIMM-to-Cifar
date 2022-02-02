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
-b=16 \
--img-size=224 \
--epochs=50 \
--color-jitter=0.4 \
--sched='cosine' \
--mean 0.5071 0.4867 0.4408 \
--std 0.2675 0.2565 0.2761 \
--model-ema --model-ema-decay=0.99 \
--reprob=0.05 --smoothing=0.1 \
--pretrained \
--lr=2e-3 \
--model=tf_efficientnet_b7_ns \
--opt=adam \
--amp \
--log-wandb \
--experiment='CF100-EFB7'

```
