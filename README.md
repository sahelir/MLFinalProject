# ML Final Project

## Dev Setup

Use `jupyter/scipy-notebook` so the notebook has the packages it needs.

Make sure Docker Desktop is running, then start the notebook container:

```bash
docker pull jupyter/scipy-notebook
docker run -it --name jupyter -p 8888:8888 -v $(pwd):/home/jovyan/work jupyter/scipy-notebook start-notebook.sh --NotebookApp.token=''
```

Then connect to the local Jupyter server from VS Code and select the Python 3 kernel.

To restart the container later:

```bash
docker start jupyter
```

To stop it:

```bash
docker stop jupyter
```

All project files should be saved in `/home/jovyan/work`, which is mapped to this repo directory on your machine.

If you need to copy a file out of Docker manually:

```bash
docker cp jupyter:/home/jovyan/work/<FILE_NAME> .
```