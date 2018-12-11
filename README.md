# Commands
#IXPUG 2018
- hwloc command:  with -X GUI use `lstop` to show the toloplogy of underlying chip (test)
- `numactl -C 1,69 ./sharing`  with openmp should improve the performance if you use two openmp threads with two logical CPUs sharing the same L1 Cash.  Check hwloc `lstop` to see the structure of your chip.
#bashrc
- ssh to your remote machine without running .bashrc `ssh -t ?:.?.?.?  /bin/sh`
- delete all files in directory with a certain extension `find . -name "*.o" -type f -delete`

