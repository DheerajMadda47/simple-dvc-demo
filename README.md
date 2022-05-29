create env 

```bash
conda create -n dvc_demo python=3.7 -y
```

activate env
```bash
conda activate dvc_demo
```

created a req file

install the req
```bash
pip install -r requirements.txt
```
download the data from 

https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5?usp=sharing

```bash
git init
```
```bash
dvc init 
```
```bash
dvc add pseudo_remote_resource/winequality.csv
```
```bash
git add .
```
```bash
git commit -m "first commit"
```

oneliner updates  for readme

```bash
git add . && git commit -m "update Readme.md"
```
```bash
git remote add origin <repo link>
git branch -M main
git push origin main
```


```bash
python3 src/load_data.py
python3 src/split_data.py
python3 src/train_and_evaluate.py
dvc repro
```


tox command -
```bash
tox
```
for rebuilding -
```bash
tox -r 
```
pytest command
```bash
pytest -v
```

setup commands -
```bash
pip install -e . 
```

build your own package commands- 
```bash
python setup.py sdist bdist_wheel
```


:::Bonus:::
Added MLFlow -> See the branch "mlflow"

create a folder named "artifacts"

mlflow server command -

```bash
mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./artifacts --host 0.0.0.0 -p 1234
```