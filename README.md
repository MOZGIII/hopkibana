# hopkibana

A docker image to export and import kibana's "saved objects" from the command line.

## Usage

### Export

```shell
docker run --rm -it -v "$PWD:/out" mozgiii/hopkibana export http://elasticsearch:9200 /out/export.json
```

or via stdout:

```shell
docker run --rm -it mozgiii/hopkibana export http://elasticsearch:9200 $
```

### Import

```shell
docker run --rm -it -v "$PWD:/out" mozgiii/hopkibana import http://elasticsearch:9200 /out/export.json
```

or from stdin:

```shell
cat export.json | docker run --rm -it mozgiii/hopkibana import http://elasticsearch:9200 $
```
