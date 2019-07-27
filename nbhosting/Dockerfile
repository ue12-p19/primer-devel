# --------
# using scipy, it's kinda big but that should not be a problem
# base-notebook lacks at least numpy, widgets, so...
FROM nbhosting/scipy-notebook

RUN jupyter nbextension enable splitcell/splitcell

RUN pip install --pre rise

RUN pip install nbautoeval ipythontutor

### git tools
RUN pip install git+https://github.com/parmentelat/nbgitpuller@nbhosting && jupyter serverextension enable --py nbgitpuller
RUN jupyter labextension install @jupyterlab/git && pip install --upgrade jupyterlab-git && jupyter serverextension enable --py jupyterlab_git
