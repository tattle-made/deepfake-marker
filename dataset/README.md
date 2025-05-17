### Steps to run the notebooks

1. Move to directory of your choice, we'll take coqui as our example.
```shell
cd ./coqui
```

2. Install and Set Up uv
```shell
pip install uv
```

3. Create a Virtual Environment Using uv

```shell
uv venv
```

4. Activate Virtual Environment

```shell
source .venv/bin/activate
```

5. Install Packages from requirements.txt Using uv

```shell
uv pip install -r requirements.txt
```

6. Run Jupyter notebook 

```shell
jupyter lab
```

6. Run all the shells in the notebook to generate audio files.