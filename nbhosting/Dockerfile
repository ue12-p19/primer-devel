# --------
# using scipy, it's kinda big but that should not be a problem
# base-notebook lacks at least numpy, widgets, so...
FROM nbhosting/scipy-notebook

RUN pip install --pre rise


### speed up jupyter lab startup
RUN jupyter lab build
