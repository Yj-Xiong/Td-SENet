# Enhancing Local Modeling and High-Frequency Band Utilization on Dual-Path Speech Denoising

## The base model is from CMGAN: Conformer-based Metric GAN for speech enhancement (https://arxiv.org/abs/2203.15149)
## How to train:
Our all codes will be released after accepting!
### Step 1:
In src:

```pip install -r requirement```

### Step 2:
Download VCTK-DEMAND dataset with 16 kHz, change the dataset dir:
```
-VCTK-DEMAND/
  -train/
    -noisy/
    -clean/
  -test/
    -noisy/
    -clean/
```

### Step 3:
If you want to train the model, run train.py
```
python3 train.py --data_dir "/home/xyj/dataset/Voicebank/noisy-vctk-16k"
### Step 4:
Evaluation with the best ckpt, if adopting PCS just evaluating with the same ckpt:
```
python3 evaluation.py --test_dir </home/xyj/dataset/Voicebank/noisy-vctk-16k> --model_path </home/xyj/CMGAN-V1/src/ckpt/>

python3 pcs_eva.py --test_dir </home/xyj/dataset/Voicebank/noisy-vctk-16k> --model_path </home/xyj/CMGAN-V1/src/ckpt/>
```
