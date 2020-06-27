FROM nvcr.io/nvidia/cuda:10.1-cudnn7-devel-centos7

# install python3
RUN yum install -y python3

# get & install pip
RUN curl https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py
RUN python2 /tmp/get-pip.py && python3 /tmp/get-pip.py

# install requirements
RUN pip2 --no-cache-dir install jupyter notebook keras sklearn pandas numpy matplotlib
RUN pip3 --no-cache-dir install jupyter notebook keras sklearn pandas numpy matplotlib

RUN pip2 install torch==1.5.1+cu101 torchvision==0.6.1+cu101 -f https://download.pytorch.org/whl/torch_stable.html
RUN pip3 install torch==1.5.1+cu101 torchvision==0.6.1+cu101 -f https://download.pytorch.org/whl/torch_stable.html

CMD ["/bin/bash"]