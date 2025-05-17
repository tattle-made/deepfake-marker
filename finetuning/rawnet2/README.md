## Finetuning Rawnet2 pretrained on ASVspoof2021

This project uses a MobileNet model pretrained on ImageNet and fine-tunes it on the [Deepfake-Eval-2024 dataset](https://huggingface.co/datasets/nuriachandra/Deepfake-Eval-2024). The [metadata](https://huggingface.co/datasets/nuriachandra/Deepfake-Eval-2024/resolve/main/audio-metadata-publish.csv) provides information about the audio files used in the dataset.

## About Rawnet2 

RawNet2 is a deep neural network architecture designed for processing raw audio waveforms directly, without relying on handcrafted features like spectrograms. It is primarily used for speaker verification and other audio-related tasks. RawNet2 improves upon its predecessor (RawNet) by incorporating more efficient residual blocks, better normalization techniques, and enhanced training strategies to increase accuracy and robustness.


### Steps to run the model

1. Install and Set Up uv
```shell
pip install uv
```

2. Create a Virtual Environment Using uv

```shell
uv venv
```

3. Activate Virtual Environment

```shell
source .venv/bin/activate
```

4. Install Packages from requirements.txt Using uv

```shell
uv pip install -r requirements.txt
```

5. Run Jupyter notebook 

```shell
jupyter lab
```

6. Run all the shells in the notebook to finetune the model.


