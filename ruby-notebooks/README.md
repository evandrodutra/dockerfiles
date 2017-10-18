# ruby-notebooks

[Docker Hub](https://hub.docker.com/r/evandrodutra/ruby-notebooks/)

## Usage

```bash
docker pull evandrodutra/ruby-notebooks
docker run -d -p 8888:8888 -v "$(pwd):/notebooks" evandrodutra/ruby-notebooks start-notebook.sh --NotebookApp.base_url=/notebooks
```

Access in your browser [docker.local:8888/notebooks](http://docker.local:8888/notebooks/tree)
