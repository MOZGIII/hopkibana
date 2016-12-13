# hopkibana

A docker image to export and import kibana's "saved objects" from the command line.

## Usage

```shell
docker run --rm -it -v "$PWD:/out" mozgiii/hopkibana export http://elasticsearch:9200 /out/export.json
```

```shell
docker run --rm -it -v "$PWD:/out" mozgiii/hopkibana import http://elasticsearch:9200 /out/export.json
```
