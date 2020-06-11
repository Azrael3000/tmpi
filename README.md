# tmpi
Run multiple MPI processes as a grid in a new tmux window and multiplex keyboard input to all of them.

## Dependencies
- [tmux](https://github.com/tmux/tmux/wiki)
- [OpenMPI](https://www.open-mpi.org/)

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

## Full usage:
See `usage()` in the [script](tmpi)

## Contributors:
* Benedikt Morbach
* Arno Mayrhofer
* Fabio Luporini
