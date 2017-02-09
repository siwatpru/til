# Run macro on every visual selected lines

1. Select lines in visual mode
2. Hit `:` to produce `:'<,'>` on the command line
3. Type `normal` follow by the register

```
:'<,'>normal @q
```

