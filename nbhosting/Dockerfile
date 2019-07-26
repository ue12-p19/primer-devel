# --------
# using scipy, it's kinda big but that should not be a problem
# base-notebook lacks at least numpy, widgets, so...
FROM nbhosting/scipy-notebook

RUN jupyter nbextension enable splitcell/splitcell

RUN pip install --pre rise

RUN pip install nbautoeval ipythontutor
