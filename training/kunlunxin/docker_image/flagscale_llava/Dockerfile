FROM zhiyuan_flagscale_llava:latest
RUN /bin/bash -c "pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple"
RUN /bin/bash -c "uname -a"
RUN /bin/bash -c alias python3=python
ENV PATH /root/miniconda/envs/python39_torch201_cuda/bin:$PATH

RUN cp /opt/ssh.tar ~/ && cd ~/ && tar -xvf ssh.tar
