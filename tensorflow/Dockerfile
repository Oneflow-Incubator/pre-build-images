FROM nvcr.io/nvidia/cuda:10.1-cudnn7-devel-centos7

# install python3
RUN yum install -y python3

# get & install pip
RUN curl https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py
RUN python2 /tmp/get-pip.py && python3 /tmp/get-pip.py

# install requirements
RUN pip2 --no-cache-dir install jupyter notebook keras sklearn pandas numpy matplotlib \ 
    tensorflow-gpu==1.15

RUN pip3 --no-cache-dir install jupyter notebook keras sklearn pandas numpy matplotlib \ 
    tensorflow-gpu==1.15

# clean cache
RUN yum clean all

# mkdir
RUN mkdir /dataset /workspace /logs

EXPOSE 8888
CMD ["/bin/bash"]