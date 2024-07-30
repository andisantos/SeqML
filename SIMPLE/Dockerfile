FROM pytorch/pytorch:1.8.1-cuda10.2-cudnn7-runtime

ENV PATH="/root/miniconda3/bin:${PATH}"
ARG PATH="/root/miniconda3/bin:${PATH}"

RUN apt-get update && \
    apt-get install --yes \
    gcc wget vim \
    git build-essential python3-pip \
    && apt-get upgrade -y libstdc++6

#RUN wget https://repo.anaconda.com/miniconda/Miniconda3-py38_23.5.2-0-Linux-x86_64.sh \
#    && mkdir /root/.conda \
#    && bash Miniconda3-py38_23.5.2-0-Linux-x86_64.sh -b \
#    && rm -f Miniconda3-py38_23.5.2-0-Linux-x86_64.sh
# RUN conda install pytorch==1.8.0 torchvision==0.9.0 torchaudio==0.8.0 cudatoolkit=10.2 -c pytorch

COPY . /src
RUN pip3 install -r /src/requirements.txt
