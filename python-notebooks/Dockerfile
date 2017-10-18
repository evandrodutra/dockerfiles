FROM jupyter/minimal-notebook

MAINTAINER Evandro Dutra <evandro.eld@gmail.com>

USER root

RUN apt-get update && apt-get install -yq \
    libav-tools \
    gcc && apt-get clean && cd ~
    rm -rf /var/lib/apt/lists/*

USER $NB_USER

RUN conda install --quiet --yes \
    'nomkl' \
    'ipywidgets=7.0*' \
    'pandas=0.19*' \
    'numexpr=2.6*' \
    'matplotlib=2.0*' \
    'scipy=0.19*' \
    'scikit-learn=0.18*' \
    'scikit-image=0.12*' \
    'sympy=1.0*' \
    'patsy=0.4*' \
    'statsmodels=0.8*' \
    'dill=0.2*' \
    'numba=0.31*' \
    'bokeh=0.12*' \
    'hdf5=1.8.17' \
    'h5py=2.6*' \
    'vincent=0.4.*' \
    'protobuf=3.*' \
    'xlrd'  && \
    conda remove --quiet --yes --force qt pyqt && \
    conda clean -tipsy && \
    jupyter nbextension enable --py widgetsnbextension --sys-prefix && \
    fix-permissions $CONDA_DIR

RUN cd /tmp && \
    git clone https://github.com/PAIR-code/facets.git && \
    cd facets && \
    jupyter nbextension install facets-dist/ --sys-prefix && \
    rm -rf facets && \
    fix-permissions $CONDA_DIR

ENV XDG_CACHE_HOME /home/$NB_USER/.cache/
RUN MPLBACKEND=Agg python -c "import matplotlib.pyplot" && \
    fix-permissions /home/$NB_USER

USER $NB_USER
