putty 다운로드해서 리눅스 환경에서 aws 접속하기

~ : 현재 디렉토리
vi 에디터가 나옴
a:add
i:insert
':w' 기록하라
make : compile

git clone https://github.com/pjreddie/darknet.git

vi Makefile

CUDA 사용 GPU=1

opencv 사용 OPENCV=1

make

wget https://pjreddie.com/media/files/yolov3.weights

./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg

---

jupyter notebook --generate-config

python3
from notebook.auth import passwd
passwd()

vim ~/.jupyter/jupyter_notebook_config.py

c = get_config()

c.NotebookApp.password = u'sha1:8'

노트북 실행