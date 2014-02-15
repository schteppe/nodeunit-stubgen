nodeunit-stubgen
================

Creates stubs for nodeunit given YUIDoc documented code.

Say you have the following structure of files:
```
docs/
    data.json  # files generated by YUIDoc
    index.html
    ...
src/
    dirA/
        MyClassA.js
    dirB/
        MyClassB.js
```

Now run
```sh
$ nodeunit-stubgen --yuiroot src --root src --outDir test docs/data.json
```

Like magic, you have now got a new folder.
```
test/
    dirA/
        MyClassA.js
    dirB/
        MyClassB.js
    index.js
```
Directory and file structure is the same, with addition to index.js, which is the main test entry file. All documented methods are stubs in the files.

For help, run ```nodeunit-stubgen --help```.
