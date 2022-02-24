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

Output of `opam exec -- dune build @@default --verbose`:

``` bash
Workspace root: /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro
Running[0]: /usr/bin/nproc > /tmp/duneb72860.output 2> /dev/null
Auto-detected concurrency: 4
disable binary cache
Running[1]: /usr/bin/ocamlc.opt -config > /tmp/dune609ab2.output
Dune context:
 { name = "default"
 ; kind = "default"
 ; profile = Dyn
 ; merlin = true
 ; for_host = None
 ; fdo_target_exe = None
 ; build_dir = "default"
 ; toplevel_path =
     Some
       External
         "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/toplevel"
 ; ocaml_bin = External "/usr/bin"
 ; ocaml = Ok External "/usr/bin/ocaml"
 ; ocamlc = External "/usr/bin/ocamlc.opt"
 ; ocamlopt = Ok External "/usr/bin/ocamlopt.opt"
 ; ocamldep = Ok External "/usr/bin/ocamldep.opt"
 ; ocamlmklib = Ok External "/usr/bin/ocamlmklib.opt"
 ; env =
     map
       { "DUNE_OCAML_HARDCODED" :
           "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib"
       ; "DUNE_OCAML_STDLIB" : "/usr/lib/ocaml"
       ; "DUNE_SOURCEROOT" :
           "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro"
       ; "INSIDE_DUNE" :
           "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_build/default"
       ; "OCAMLFIND_IGNORE_DUPS_IN" :
           "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_build/install/default/lib"
       ; "OCAMLPATH" :
           "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_build/install/default/lib"
       ; "OCAMLTOP_INCLUDE_PATH" :
           "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_build/install/default/lib/toplevel"
       ; "OCAML_COLOR" : "always"
       ; "OPAMCOLOR" : "always"
       }
 ; findlib_path =
     [ External
         "/home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib"
     ]
 ; arch_sixtyfour = true
 ; natdynlink_supported = true
 ; supports_shared_libraries = true
 ; ocaml_config =
     { version = "4.13.1"
     ; standard_library_default = "/usr/lib/ocaml"
     ; standard_library = "/usr/lib/ocaml"
     ; standard_runtime = "the_standard_runtime_variable_was_deleted"
     ; ccomp_type = "cc"
     ; c_compiler = "gcc"
     ; ocamlc_cflags =
         [ "-O2"
         ; "-fno-strict-aliasing"
         ; "-fwrapv"
         ; "-pthread"
         ; "-fPIC"
         ; "-march=x86-64"
         ; "-mtune=generic"
         ; "-O2"
         ; "-pipe"
         ; "-fno-plt"
         ]
     ; ocamlc_cppflags = [ "-D_FILE_OFFSET_BITS=64"; "-D_FORTIFY_SOURCE=2" ]
     ; ocamlopt_cflags =
         [ "-O2"
         ; "-fno-strict-aliasing"
         ; "-fwrapv"
         ; "-pthread"
         ; "-fPIC"
         ; "-march=x86-64"
         ; "-mtune=generic"
         ; "-O2"
         ; "-pipe"
         ; "-fno-plt"
         ]
     ; ocamlopt_cppflags =
         [ "-D_FILE_OFFSET_BITS=64"; "-D_FORTIFY_SOURCE=2" ]
     ; bytecomp_c_compiler =
         [ "gcc"
         ; "-O2"
         ; "-fno-strict-aliasing"
         ; "-fwrapv"
         ; "-pthread"
         ; "-fPIC"
         ; "-march=x86-64"
         ; "-mtune=generic"
         ; "-O2"
         ; "-pipe"
         ; "-fno-plt"
         ; "-D_FILE_OFFSET_BITS=64"
         ; "-D_FORTIFY_SOURCE=2"
         ]
     ; bytecomp_c_libraries = [ "-lm"; "-ldl"; "-lpthread" ]
     ; native_c_compiler =
         [ "gcc"
         ; "-O2"
         ; "-fno-strict-aliasing"
         ; "-fwrapv"
         ; "-pthread"
         ; "-fPIC"
         ; "-march=x86-64"
         ; "-mtune=generic"
         ; "-O2"
         ; "-pipe"
         ; "-fno-plt"
         ; "-D_FILE_OFFSET_BITS=64"
         ; "-D_FORTIFY_SOURCE=2"
         ]
     ; native_c_libraries = [ "-lm"; "-ldl" ]
     ; cc_profile = []
     ; architecture = "amd64"
     ; model = "default"
     ; int_size = 63
     ; word_size = 64
     ; system = "linux"
     ; asm = [ "as" ]
     ; asm_cfi_supported = true
     ; with_frame_pointers = false
     ; ext_exe = ""
     ; ext_obj = ".o"
     ; ext_asm = ".s"
     ; ext_lib = ".a"
     ; ext_dll = ".so"
     ; os_type = "Unix"
     ; default_executable_name = "a.out"
     ; systhread_supported = true
     ; host = "x86_64-pc-linux-gnu"
     ; target = "x86_64-pc-linux-gnu"
     ; profiling = false
     ; flambda = false
     ; spacetime = false
     ; safe_string = false
     ; exec_magic_number = "Caml1999X030"
     ; cmi_magic_number = "Caml1999I030"
     ; cmo_magic_number = "Caml1999O030"
     ; cma_magic_number = "Caml1999A030"
     ; cmx_magic_number = "Caml1999Y030"
     ; cmxa_magic_number = "Caml1999Z030"
     ; ast_impl_magic_number = "Caml1999M030"
     ; ast_intf_magic_number = "Caml1999N030"
     ; cmxs_magic_number = "Caml1999D030"
     ; cmt_magic_number = "Caml1999T030"
     ; natdynlink_supported = true
     ; supports_shared_libraries = true
     ; windows_unicode = false
     }
 }
Actual targets:
- alias @@default
Running[2]: (cd _build/default && /usr/bin/ocamlc.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -w -49 -nopervasives -nostdlib -g -bin-annot -I src/view/.view.objs/byte -no-alias-deps -opaque -o src/view/.view.objs/byte/view.cmo -c -impl src/view/view.ml-gen)
Running[3]: (cd _build/default && /usr/bin/ocamlc.opt -g -w -24 -I .ppx/510f92ba3c7471c61121a87d4dd403ff -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/ppx -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ocaml-compiler-libs/common -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ocaml-compiler-libs/shadow -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppx_derivers -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/ast -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/astlib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/print_diff -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/stdppx -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/traverse_builtins -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/sexplib0 -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/stdlib-shims -I /usr/lib/ocaml/compiler-libs -no-alias-deps -o .ppx/510f92ba3c7471c61121a87d4dd403ff/dune__exe___ppx.cmo -c -impl .ppx/510f92ba3c7471c61121a87d4dd403ff/_ppx.ml-gen)
Running[4]: (cd _build/default/.js/stdlib && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o std_exit.cmo.js /usr/lib/ocaml/std_exit.cmo)
Running[5]: (cd _build/default/src && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml build-runtime --pretty --source-map-inline -o app.bc.runtime.js /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ojs/ojs_runtime.js)
Running[6]: (cd _build/default && /usr/bin/ocamlopt.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -w -49 -nopervasives -nostdlib -g -I src/view/.view.objs/byte -I src/view/.view.objs/native -intf-suffix .ml-gen -no-alias-deps -opaque -o src/view/.view.objs/native/view.cmx -c -impl src/view/view.ml-gen)
Running[7]: (cd _build/default && /usr/bin/ocamlopt.opt -g -w -24 -I .ppx/510f92ba3c7471c61121a87d4dd403ff -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/ppx -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ocaml-compiler-libs/common -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ocaml-compiler-libs/shadow -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppx_derivers -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/ast -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/astlib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/print_diff -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/stdppx -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/traverse_builtins -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/sexplib0 -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/stdlib-shims -I /usr/lib/ocaml/compiler-libs -intf-suffix .ml-gen -no-alias-deps -o .ppx/510f92ba3c7471c61121a87d4dd403ff/dune__exe___ppx.cmx -c -impl .ppx/510f92ba3c7471c61121a87d4dd403ff/_ppx.ml-gen)
Running[8]: (cd _build/default && /usr/bin/ocamlopt.opt -g -w -24 -o .ppx/510f92ba3c7471c61121a87d4dd403ff/ppx.exe /usr/lib/ocaml/compiler-libs/ocamlcommon.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ocaml-compiler-libs/common/ocaml_common.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/astlib/astlib.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/stdlib-shims/stdlib_shims.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/ast/ppxlib_ast.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ocaml-compiler-libs/shadow/ocaml_shadow.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/print_diff/ppxlib_print_diff.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppx_derivers/ppx_derivers.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/traverse_builtins/ppxlib_traverse_builtins.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/sexplib0/sexplib0.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/stdppx/stdppx.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ppxlib/ppxlib.cmxa /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/ppx/jsoo_react_ppx.cmxa .ppx/510f92ba3c7471c61121a87d4dd403ff/dune__exe___ppx.cmx)
Running[9]: (cd _build/default/.js/js_of_ocaml && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o js_of_ocaml.cma.js /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/js_of_ocaml/js_of_ocaml.cma)
Running[10]: (cd _build/default/.js/jsoo-react.lib && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o react.cma.js /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/lib/react.cma)
Running[11]: (cd _build/default/.js/ojs && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o ojs.cma.js /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ojs/ojs.cma)
Running[12]: (cd _build/default/.js/stdlib && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o stdlib.cma.js /usr/lib/ocaml/stdlib.cma)
Running[13]: (cd _build/default && .ppx/510f92ba3c7471c61121a87d4dd403ff/ppx.exe --cookie 'library-name="view"' -o src/view/main.pp.ml --impl src/view/main.ml -corrected-suffix .ppx-corrected -diff-cmd - -dump-ast)
Running[14]: (cd _build/default && .ppx/510f92ba3c7471c61121a87d4dd403ff/ppx.exe -o src/app.pp.ml --impl src/app.ml -corrected-suffix .ppx-corrected -diff-cmd - -dump-ast)
Running[15]: (cd _build/default && /usr/bin/ocamldep.opt -modules -impl src/view/main.pp.ml) > _build/default/src/view/.view.objs/main.pp.ml.d
Running[16]: (cd _build/default && /usr/bin/ocamlc.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -bin-annot -I src/view/.view.objs/byte -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/js_of_ocaml -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/lib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ojs -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/uchar -no-alias-deps -opaque -open View -o src/view/.view.objs/byte/view__Main.cmo -c -impl src/view/main.pp.ml)
Running[17]: (cd _build/default && /usr/bin/ocamlc.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -a -o src/view/view.cma src/view/.view.objs/byte/view.cmo src/view/.view.objs/byte/view__Main.cmo)
Running[18]: (cd _build/default && /usr/bin/ocamlopt.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -I src/view/.view.objs/byte -I src/view/.view.objs/native -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/js_of_ocaml -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/lib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ojs -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/uchar -intf-suffix .ml -no-alias-deps -opaque -open View -o src/view/.view.objs/native/view__Main.cmx -c -impl src/view/main.pp.ml)
Running[19]: (cd _build/default && /usr/bin/ocamlc.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -bin-annot -I src/.app.eobjs/byte -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/js_of_ocaml -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/lib -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ojs -I /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/uchar -I src/view/.view.objs/byte -no-alias-deps -opaque -o src/.app.eobjs/byte/dune__exe__App.cmo -c -impl src/app.pp.ml)
Running[20]: (cd _build/default/src/view && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o .view.objs/view.cma.js view.cma)
Output[18]:
File "_none_", line 1:
Warning 58 [no-cmx-file]: no cmx file was found in path for module React, and its interface was not compiled with -opaque
File "_none_", line 1:
Warning 58 [no-cmx-file]: no cmx file was found in path for module React__Dom_html, and its interface was not compiled with -opaque
Running[21]: (cd _build/default/src && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml --pretty --source-map-inline -o .app.eobjs/byte/dune__exe__App.cmo.js .app.eobjs/byte/dune__exe__App.cmo)
Running[22]: (cd _build/default && /usr/bin/ocamlc.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -o src/app.bc /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/js_of_ocaml/js_of_ocaml.cma /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/ojs/ojs.cma /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/lib/jsoo-react/lib/react.cma src/view/view.cma src/.app.eobjs/byte/dune__exe__App.cmo)
Running[23]: (cd _build/default && /usr/bin/ocamlopt.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -a -o src/view/view.cmxa src/view/.view.objs/native/view.cmx src/view/.view.objs/native/view__Main.cmx)
Running[24]: (cd _build/default && /usr/bin/ocamlopt.opt -w @1..3@5..28@30..39@43@46..47@49..57@61..62-40 -strict-sequence -strict-formats -short-paths -keep-locs -g -shared -linkall -I src/view -o src/view/view.cmxs src/view/view.cmxa)
Running[25]: (cd _build/default/src && /home/glennsl/dev/temp/jsoo-react-no-cmx-file-repro/_opam/bin/js_of_ocaml link --source-map-inline -o app.bc.js app.bc.runtime.js ../.js/stdlib/stdlib.cma.js ../.js/js_of_ocaml/js_of_ocaml.cma.js ../.js/ojs/ojs.cma.js ../.js/jsoo-react.lib/react.cma.js view/.view.objs/view.cma.js .app.eobjs/byte/dune__exe__App.cmo.js ../.js/stdlib/std_exit.cmo.js)
```
