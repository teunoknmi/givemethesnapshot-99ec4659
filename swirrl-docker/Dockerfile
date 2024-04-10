FROM 498391678517.dkr.ecr.eu-west-1.amazonaws.com/knmi/swirrl/jupyterswirrlui/knmi-datascience-jupyter-notebook@sha256:b6618a160ea3c8b9f43941f34cda9c968f355ed65d2f1d62a1aa84da1e680261
USER root
ARG NB_USER=jovyan
ARG NB_UID=1000
ENV USER ${NB_USER}
ENV NB_UID ${NB_UID}
ENV HOME /home/${NB_USER}
RUN id ${NB_USER} || adduser --disabled-password --gecos "Default user" --uid ${NB_UID} ${NB_USER}
COPY . ${HOME}
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}
WORKDIR ${HOME}
