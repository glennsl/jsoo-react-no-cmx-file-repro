# jsoo-react no-cmx-file repro

Steps to reproduce:

``` bash
git clone git@github.com:glennsl/jsoo-react-no-cmx-file-repro
cd jsoo-react-no-cmx-file-repro
make create-switch
make init
make build
```

Will output the following:

``` bash
opam exec -- dune build @@default
File "_none_", line 1:   
Warning 58 [no-cmx-file]: no cmx file was found in path for module React, and its interface was not compiled with -opaque
File "_none_", line 1:
Warning 58 [no-cmx-file]: no cmx file was found in path for module React__Dom_html, and its interface was not compiled with -opaque
```

