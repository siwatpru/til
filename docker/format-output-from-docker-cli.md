# Format output from docker CLI

Output from various commands of Docker CLI can be manipulated with
[Go templates](https://golang.org/pkg/text/template/) using `--format`.


Normal `docker ps` output

```
> docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                    NAMES
3fe2829131c6        ghost:latest        "/entrypoint.sh npm s"   4 days ago          Up 17 seconds       0.0.0.0:2368->2368/tcp   ghost
```

If we want only `Names` and `Command`, we can use:

```
> docker ps --format "{{.Names}}\t{{.Command}}"
ghost "/entrypoint.sh npm s"
```

Output can be manupulated by template functions:

```
> docker ps --format "{{title .Names}}\t{{upper .Command}}"
Ghost "/ENTRYPOINT.SH NPM S"
```

More info on template functions at
[https://docs.docker.com/engine/admin/formatting/](https://docs.docker.com/engine/admin/formatting/)
