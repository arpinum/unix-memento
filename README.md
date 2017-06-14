# Unix Memento
Collection of Unix quick tips

## Run command, display result and save output to a file

```
./script.sh 2>&1 | tee result.txt
```

## Rename multiple files

```
rename 's/this/that/g' -p -g "*.js"
```

Rename all expanded (`-g`) js files, replacing `this` by `that` and creating folder (`-p`) if needed.
