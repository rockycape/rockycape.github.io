---
layout: page
title: "JupyterLab"
---

**quickedit copy/paste with mouse with "Bash on Ubuntu on Windows" prompt**
Within WSL the right mouse button is copy when there is a selected text, and the same button is paste when there is something in the clipboard, no mater it is copied within the WSL window or within another Windows application.

**install WSL & JupyterLab on my windows 10 PC**  
step 01 - install WSL (Windows Subsystem For Linux (Ubuntu))  
step 02 - open "Bash on Ubuntu on Windows" prompt  
step 03 - type:  
```
pip install jupyterlab
```

**start JupyterLab**
It's a good idea to change directory to a project folder before starting JupyterLab as it creates several files

```
jupyter-lab --no-browser
```

**exit JupyterLab**

```
Use Control-C to stop this server and shut down all kernels (twice to skp confirmation)
```
