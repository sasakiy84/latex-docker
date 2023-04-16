ある程度うまくいくコマンド

```
docker container run -it --rm -v $PWD:/data pandoc/core:latest-alpine --from=markdown+ignore_line_breaks --to=latex --number-sections --top-level-division=chapter -o /data/main.tex main.md
docker run --rm -it -v $PWD:/workdir paperist/texlive-ja:latest sh -c 'lualatex main.tex'
```
