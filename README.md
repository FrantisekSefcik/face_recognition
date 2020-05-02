# Face recognition
Author: František Šefčík

### Instalation

1. Clone repository
```shell script
git clone git@github.com:FrantisekSefcik/face_recognition.git
```

2. Build docker image
```shell script
cd cd face_recognition
docker build -t face-recognition/tensorflow:2.1.0-gpu-py3-jupyter .
```

3. Run docker container
```shell script
cd ..
docker run --gpus all -u $(id -u):$(id -g) --rm -p 8888:8888 -p 6006:6006 -v $(pwd):/project -it --name face-recognition-project face-recognition/tensorflow:2.1.0-gpu-py3-jupyter
```