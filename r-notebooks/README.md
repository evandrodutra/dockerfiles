# r-notebooks

[Docker Hub](https://hub.docker.com/r/evandrodutra/r-notebooks/)

## Usage

```bash
docker pull evandrodutra/r-notebooks
docker run -d -p 8888:8888 -v "$(pwd)/notebooks:/home/jovyan/work" evandrodutra/r-notebooks start-notebook.sh --NotebookApp.token='' --NotebookApp.base_url=/
```

Access in your browser [docker.local:8888/](http://docker.local:8888/tree)
