# Ignore further changes to a file

To ignore further changes to a file currently in the repository use:

```
git update-index --assume-unchanged path/to/file
```

To restore:

```
git update-index --no-assume-unchanged path/to/file
```

