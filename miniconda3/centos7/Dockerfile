FROM centos:centos7
MAINTAINER Continuum Analytics, Inc. <conda@continuum.io>

RUN yum -y update \
    && yum -y install curl bzip2 \
    && curl -sSL https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -o /tmp/miniconda.sh \
    && bash /tmp/miniconda.sh -bfp /usr/local/ \
    && rm -rf /tmp/miniconda.sh \
    && conda install -y python=3 conda=4.3.21 \
    && conda clean --all --yes \
    && rpm -e --nodeps curl bzip2 \
    && yum clean all
