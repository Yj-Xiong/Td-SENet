# Td-SENet: A Triple-decoder Network for High-quality Speech Enhancement under Low-SNR Conditions
All codes will be released after accepting!
## The base model is from CMGAN: Conformer-based Metric GAN for speech enhancement (https://arxiv.org/abs/2203.15149)

## Demons are available in Demos directory
### A4_204.wav file in THCHS-30 dev set
### B7_278.wav file in THCHS-30 dev set
### C23_628.wav file in THCHS-30 dev set
## How to train:
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

### Step 3: Training
If you want to train the model, run train.py
```
python3 train.py --data_dir "/home/xyj/dataset/Voicebank/noisy-vctk-16k"
```
## Inferencing and Evaluating
python3 evaluation.py --test_dir </home/xyj/dataset/Voicebank/noisy-vctk-16k> --model_path </home/xyj/CMGAN-V1/src/ckpt/>

```
