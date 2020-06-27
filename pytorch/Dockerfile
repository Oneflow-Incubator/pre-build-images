FROM tensorflow/tensorflow:devel-py3

RUN apt-get update -y \
    && pip install jupyter notebook keras sklearn pandas numpy matplotlib -i https://pypi.tuna.tsinghua.edu.cn/simple \
    && wget https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow_cpu-2.1.0-cp36-cp36m-manylinux2010_x86_64.whl \
    && pip install ./tensorflow_cpu-2.1.0-cp36-cp36m-manylinux2010_x86_64.whl \
    && rm -f ./tensorflow_cpu-2.1.0-cp36-cp36m-manylinux2010_x86_64.whl \
    && mkdir /dataset \
    && mkdir /workspace \
    && mkdir /logs
# COPY prepare.sh /root/.jupyter/prepare.sh
# RUN chmod +x /root/.jupyter/prepare.sh

# ENV PATH=$PATH:/usr/local/bin

VOLUME /dataset
VOLUME /workspace
VOLUME /logs

EXPOSE 8888
CMD ["/bin/bash"]