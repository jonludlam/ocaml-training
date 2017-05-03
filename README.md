To prepare:

```
aptitude install ipython-notebook libzmq3-dev jupyter-core jupyter-client jupyter-notebook
opam install iocaml rpc

cat > `opam config var share`/iocaml/kernel.json.tmp << EOF
{
 "display_name": "OCaml",
 "language": "ocaml",
 "argv": [
  "`opam config var bin`/iocaml.top",
  "-log",
  "iocaml.log",
  "-object-info",
  "-completion",
  "-connection-file",
  "{connection_file}"
 ]
}
EOF

sudo jupyter kernelspec install --name iocaml-kernel `opam config var share`/iocaml

```

To run:

```
jupyter notebook --Session.key='b""' notebooks/
```
