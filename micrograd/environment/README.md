# docker pull
```
sudo docker pull nvcr.io/nvidia/pytorch:22.12-py3

```



# docker create

```
xhost local:root

sudo docker run -itd  \
--name tidy-karpathy-micrograd \
--user root \
--privileged \
-p 9801:9801 \
-v /etc/localtime:/etc/localtime \
--ipc=host \
-v /tmp/.X11-unix:/tmp/.X11-unix \
-e DISPLAY=$DISPLAY \
-v /data/home/baseuser/tidy-workspace/tidy-karpathy/micrograd:/root/micrograd \
-w /root/micrograd nvcr.io/nvidia/pytorch:22.12-py3


```


# enter docker
```
xhost local:root
sudo docker stop tidy-karpathy-micrograd
sudo docker start tidy-karpathy-micrograd
sudo docker exec -it tidy-karpathy-micrograd /bin/bash

```

# install jupyter
```
pip3 install jupyter -i https://pypi.tuna.tsinghua.edu.cn/simple
cd /root/micrograd
nohup jupyter notebook --ip=0.0.0.0 --allow-root --port 9801 &


http://localhost:9801/tree

```

# install lib
```
pip3 install micrograd
pip3 install graphviz

apt updata
apt install -y graphviz 

```


# docker commit
```
> dlstreamer:2022.2-release
sudo docker commit -a "tonye" -m "install 20200109" dec65d429bac 10.9.36.17:5000/tidy-paddlepaddle/face-recognition:1.0
sudo docker inspect 10.9.36.17:5000/tidy-paddlepaddle/face-recognition:1.0



```
