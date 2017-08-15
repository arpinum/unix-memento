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


## Create bootable usb key with linux from OSX

```
hdiutil convert ubuntu.iso -format UDRW -o ubuntu
diskutil list # note your device number
diskutil unmountDisk /dev/diskX # replace X by the number
sudo dd if=ubuntu.dmg of=/dev/rdiskX bs=1m # replace X by the number
```

## Advanced file search

Find all `package.json` not in a `node_modules` directory containing text `lodash`:

```
find . -not -iwholename '*node_modules*' -name package.json -exec grep -H lodash {} \;
```


