## Finetuning MobileNet Pretrained on ImageNet

This project uses a MobileNet model pretrained on ImageNet and fine-tunes it on the [Deepfake-Eval-2024 dataset](https://huggingface.co/datasets/nuriachandra/Deepfake-Eval-2024). The [metadata](https://huggingface.co/datasets/nuriachandra/Deepfake-Eval-2024/resolve/main/audio-metadata-publish.csv) provides information about the audio files used in the dataset.

### About MobileNet

MobileNet is a lightweight and efficient convolutional neural network designed for mobile and edge devices. It is commonly used in tasks such as object detection, fine-grained classification, face attribute analysis, and image localization.

In this project, we use MobileNet to detect deepfakes in audio. We first convert the audio signals into spectrogram images and then pass them through a MobileNet-based CNN.

### Model Architecture

We use the pretrained MobileNet as a feature extractor by freezing its base layers. A custom classification head is added on top for binary classification:

```python
x = Dense(32, activation='relu')(x)
x = BatchNormalization()(x)
x = Dropout(0.5)(x)
x = GlobalAveragePooling2D()(x)
output = Dense(2, activation='sigmoid')(x)
```

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