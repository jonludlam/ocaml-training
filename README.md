Running locally
===============

1. Install [opam](https://opam.ocaml.org/doc/Install.html)
   Debian and Ubuntu are currently the best supported distributions for `opam`:
   ```
   apt-get -y install opam
   opam init -y --comp=4.02.3
   eval `opam config env`
   ```

2. Use `opam` to install `iocaml`:
   ```
   opam install -y depext   # This step isn't necessary if you have opam 1.2.2
   opam depext iocaml       # This step installs system packages which iocaml needs.  You may have to enter your password.
   opam install -y iocaml
   ```

3. Run the `iocaml` server.  This will start a server listening on localhost.   In most desktop environments it will also automatically open the notebook index in your browser: 
   ```
   iocaml notebooks/
   ```

