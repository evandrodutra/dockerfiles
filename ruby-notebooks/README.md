# ruby-notebooks

[Docker Hub](https://hub.docker.com/r/evandrodutra/ruby-notebooks/)

## Usage

```bash
docker pull evandrodutra/ruby-notebooks
docker run -d -p 8888:8888 -v "$(pwd)/notebooks:$/home/jovyan/work" evandrodutra/ruby-notebooks start-notebook.sh --NotebookApp.token='' --NotebookApp.base_url=/
```

Access in your browser [docker.local:8888/](http://docker.local:8888/tree)
