# Setting up a using the `fileupload` widget Jupyter Notebook environment via binder

[![Binder](https://beta.mybinder.org/badge.svg)](https://beta.mybinder.org/v2/gh/draperjames/fileupload2path/master?filepath=index.ipynb)

Click the binder badge above to start a new binder virtual machine.

## postBuild
```
jupyter contrib nbextension install --user
jupyter nbextension enable --py widgetsnbextension
jupyter nbextension enable python-markdown/main

# Add the fileupload module.
jupyter nbextension install --user --py fileupload
jupyter nbextension enable  --user --py fileupload

# Notebooks w/ extensions that auto-run code must be "trusted" to work the first time
jupyter trust index.ipynb
```

## requirements.txt
```
ipywidgets
jupyter_contrib_nbextensions
fileupload
```
