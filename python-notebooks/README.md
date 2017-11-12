# python-notebooks

[Docker Hub](https://hub.docker.com/r/evandrodutra/python-notebooks/)

## Usage

```bash
docker pull evandrodutra/python-notebooks
docker run -d -p 8888:8888 -v "$(pwd)/notebooks:/home/jovyan/work" evandrodutra/python-notebooks start-notebook.sh --NotebookApp.token='' --NotebookApp.base_url=/
```

Access in your browser [docker.local:8888/](http://docker.local:8888/tree)
