## Dev Setup
use jupyter/scipy-notebook since it has all the packages we need

```bash
$: docker pull jupyter/scipy-notebook 
$: docker run -it --name jupyter -p 8888:8888 jupyter/scipy-notebook
```
Then, use the localhost server url as the jupyter kernel.\
Set display name (optional)\
Select Python 3 ipykernel