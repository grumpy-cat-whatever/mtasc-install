# Instructions for compiling MTASC

## Windows: Cygwin + patched opam

1. Download and install "OCaml for Windows" from here:
   https://fdopen.github.io/opam-repository-mingw/

2. Download `setup-x86_64.exe` from https://cygwin.com/
   and save it into your OCaml folder from the previous step
   (e.g. `C:\OCaml32\`).
3. Run `setup-x86_64.exe` and install the package `perl-IPC-System-Simple`.
   Optional but recommended: Let the setup create a shortcut
   to its shell (last step of the setup).
4. You need to install ocamlfind: Open the Cygwin shell, then run 
   ```bash
   opam install ocamlfind
   ```
5. Once that's done, use ocamlfind to install extlib and camlp5: Run
   ```bash
   ocamlfind install extlib camlp5
   ```
6. Now, finally, check out this repository via git
   ```bash
   git clone https://github.com/grumpy-cat-whatever/mtasc-install.git
   ```
   Or download the source as a `*.zip` file from Github.
7. Go to the `zlib/` subdirectory and follow the instructions.
8. Clone the [ocamllibs project](https://github.com/grumpy-cat-whatever/ocamllibs) into a subdirectory.
   I kept the original name `ocaml`, but I believe any **reasonable**
   name would work:
   ```bash
   git clone https://github.com/grumpy-cat-whatever/ocamllibs.git ocaml
   ```
   Or download the source as a `*.zip` file from Github.
9. Go to the subdirectory from step 8 and clone the [mtasc project](https://github.com/grumpy-cat-whatever/mtasc)
   into a subdirectory called `mtasc` (the name is **required**).
   ```bash
   git clone https://github.com/grumpy-cat-whatever/mtasc.git mtasc
   ```
   Or download the source as a `*.zip` file from Github.
10. Your project structure should look something like this now:
    ```
    mtasc-install/
    |
    -- ocaml/
    |   |
    |   -- extc/
    |   |
    |   -- extlib-leftovers/
    |   |
    |   -- ilib/
    |   |
    |   -- javalib/
    |   |
    |   -- mtasc/
    |   |
    |   -- neko/
    |   |
    |   -- mtasc/
    |   |
    |  ...
    |
    -- zlib/ 
    ```
11. If lady fortune smiles upon you today, you should be able to run the
    following in the `mtasc-install` folder:
    ```bash
    ocaml install.ml
    ```
11. You're not that lucky. Resolve any issues from the previous steps.
    If you think that others could benefit from your experience,
    write something down and make sure people see it.
    
## Other OSes/build systems

If you are on a POSIX system, you probably won't need Cygwin.
The rest should be analogous to the instructions for Windows,
though. I think you can figure it out.

Building on Windows and not using the method I described above will
probably be very frustrating. I tried to go without Cygwin and I
really can't recommend it. Working with WSL might be relatively painless;
let me know if you have success with it.
