# Getting Started

### Train and evaluation（整理好代码并补充完整）

Take `SynLiDAR` → `SemanticPOSS` as an example,



preliminary (Source-only and Target-only)
```bash
# Source-only
python train.py --amp --fix_random_seed --cfg_file configs/fully/minknet/syn2poss_src.yaml

# Tource-only
python train.py --amp --fix_random_seed --cfg_file configs/fully/minknet/syn2poss_tgt.yaml

```

When obtained Source-only model, we can use it as a good start point and conduct experiments under source-free active domain adaptation and active domain adaption as follows:

```bash
# AL
python train_active.py --amp --fix_random_seed --cfg_file configs/al/minknet/syn2poss.yaml --set ACTIVE.ACTIVE_METHOD VCD     

# ASFDA
python train_active.py --amp --fix_random_seed --cfg_file configs/al/minknet/syn2poss.yaml --init_model_ckp "/path_to_synlidar2poss_sourceonly_checkpoint/ckp/checkpoint_epoch_10.pth" --set ACTIVE.ACTIVE_METHOD VCD

# ADA  
python train_active_da.py --amp --fix_random_seed --cfg_file configs/ada/minknet/syn2poss.yaml --init_model_ckp "/path_to_synlidar2poss_sourceonly_checkpoint/ckp/checkpoint_epoch_10.pth" --set ACTIVE.ACTIVE_METHOD VCD

```



