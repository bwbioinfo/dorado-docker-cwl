FROM rockylinux/rockylinux:9

RUN dnf install -y \
    python3 \
    python3-pip \
    python3-devel \
    gcc \
    wget \
    && dnf clean all

RUN pip3 install --upgrade pip

WORKDIR /opt

RUN wget https://cdn.oxfordnanoportal.com/software/analysis/dorado-0.4.3-linux-x64.tar.gz \
    && tar -xzf dorado-0.4.3-linux-x64.tar.gz \
    && rm dorado-0.4.3-linux-x64.tar.gz \
    && mv dorado-0.4.3-linux-x64 dorado


ENV PATH="/opt/dorado/bin:${PATH}"

CMD ["dorado"]
