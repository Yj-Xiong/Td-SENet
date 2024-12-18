# Td-SENet: A Triple-decoder Network for High-quality Speech Enhancement under Low-SNR Conditions
All codes will be released after accepting!
## The base model is from CMGAN: Conformer-based Metric GAN for speech enhancement (https://arxiv.org/abs/2203.15149)

## Demons are available
### A4_204 file in THCHS-30 dev set:
Clean audio: 
```html
<audio controls>
  <source src="https://github.com/Yj-Xiong/Td-SENet/raw/my-page/Demos/A4_204%20clean.wav" type="audio/wav">
  Your browser does not support the audio element.
</audio>
-9dB Noisy audio: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204_-9dB.wav)
“`
Enhanced by CMGAN: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204_cmgan.wav)
“`
Enhanced by Td-SENet: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204 tdnet.wav)
“`
### A4_204.wav file in THCHS-30 dev set:
Clean audio: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204 clean.wav)
“`
-9dB Noisy audio: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204_-9dB.wav)
“`
Enhanced by CMGAN: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204_cmgan.wav)
“`
Enhanced by Td-SENet: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/A4_204 tdnet.wav)
“`
### B7_278.wav file in THCHS-30 dev set:
Clean audio: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/B7_278 clean.wav)
“`
-9dB Noisy audio: “`html https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/B7_278_-9dB.wav
“`
Enhanced by CMGAN: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/B7_278_cmgan.wav)
“`
Enhanced by Td-SENet: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/B7_278 tdnet.wav)
“`
### C23_628.wav file in THCHS-30 dev set:
Clean audio: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/C23_628 clean.wav)
“`
-9dB Noisy audio: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/C23_628_-9dB.wav)
“`
Enhanced by CMGAN: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/C23_628_cmgan.wav)
“`
Enhanced by Td-SENet: “`[html\](https://github.com/Yj-Xiong/Td-SENet/edit/my-page/Demos/C23_628 tdnet.wav)
“`
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
