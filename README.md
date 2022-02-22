# tmpi
Run multiple MPI processes as a grid in a new tmux window and multiplex keyboard input to all of them.

## Dependencies
- [tmux](https://github.com/tmux/tmux/wiki)
- [Reptyr](https://github.com/nelhage/reptyr) 
- [OpenMPI](https://www.open-mpi.org/)
- [MPICH](https://www.mpich.org/)

## Installation
Just copy the `tmpi` script somewhere in your `PATH`.
One-liner:
```bash
curl https://raw.githubusercontent.com/Azrael3000/tmpi/master/tmpi -o /somewhere/in/your/path/tmpi
```

## Example usage:

Parallel debugging with GDB:
```
tmpi 4 gdb executable
```

It is advisable to run gdb with a script (e.g. `script.gdb`) so you can use
```
tmpi 4 gdb -x script.gdb executable
```

If you have a lot of processors you want to have `set pagination off` and add the `-q` argument to gdb:
```
tmpi 4 gdb -q -x script.gdb executable
```
This avoids pagination and the output of the copyright of gdb, which can be a nuissance when you have very small tmux panes.

## Full usage:
See `usage()` in the [script](tmpi)

## Contributors:
* Benedikt Morbach
* Arno Mayrhofer (Azrael3000)
* Fabio Luporini
* Shumpei Shiina (s417-lama)
