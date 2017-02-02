# Pipe stderr

To pipe stderr into other process, use I/O redirection from stderr to stdout
and then pipe into another process.

Node.js code for example

```
console.log('Hello STDOUT')
console.error('Hello STDERR')
```

To redirect stdout to file use

```
> node log.js > stdout.log
Hello STDERR
> cat stdout.log
Hello STDOUT
```

To redirect stderr to file use

```
> node log.js 2> stderr.log
Hello STDOUT
> cat stderr.log
Hello STDERR
```

Redirect stderr to stdout, so that we can pipe into another process.

```
node log.js 2>&1 >/dev/null | less
```

`2>&1` means to redirect file descriptor 2 (stderr) into file descriptor 1 (stdout)
