# r-notebooks

[Docker Hub](https://hub.docker.com/r/evandrodutra/r-notebooks/)

## Usage

```bash
docker pull evandrodutra/r-notebooks
docker run -d -p 8888:8888 -v "$(pwd):/notebooks" evandrodutra/r-notebooks start-notebook.sh --NotebookApp.base_url=/notebooks
```

Access in your browser [docker.local:8888/notebooks](http://docker.local:8888/notebooks/tree)
