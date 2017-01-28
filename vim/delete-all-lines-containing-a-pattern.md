# Delete all lines containing a pattern

Using the command `:g` we can find lines containing a pattern and use
`/d` command to delete them.

---

To delete lines containg the word `unused`:
```
:g/unused/d
```

To delete all the do _not_ contain a pattern, use `g!`:
```
:g!/important/d
```

`\|` can be used to delete lines matching multiple keywords.
```
:g/unused\|unused_too/d
```

Current search results from `/` or `*` can be delete with:
```
:g//d
```
