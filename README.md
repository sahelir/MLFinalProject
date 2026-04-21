## Dev Setup

### Initialization
use jupyter/scipy-notebook since it has all the packages we need\

**Make sure Docker Desktop is opened**
```bash
$: docker pull jupyter/scipy-notebook 
$: docker run -it --name jupyter -p 8888:8888 -v $(pwd):/home/jovyan/work jupyter/scipy-notebook start-notebook.sh --NotebookApp.token=''
```
Then, use the localhost server url as the jupyter kernel. (top right corner of the notebook if you are using vscode)\
Set display name (optional)\
Select Python 3 ipykernel

### Starting Container
```bash
$: docker start jupyter
```
this will start the container and expose the server

### Cleanup Container
```bash
$: docker stop jupyter
```
this will stop the docker container

!! Make sure you are saving and accessing files in the work/ directory. \
work/ is where all the code and data are (you can think of it as a renamed MLFinalProject directory) !!