# Commands
#IXPUG 2018
- hwloc command:  with -X GUI use `lstop` to show the toloplogy of underlying chip (test)
- `numactl -C 1,69 ./sharing`  with openmp should improve the performance if you use two openmp threads with two logical CPUs sharing the same L1 Cash.  Check hwloc `lstop` to see the structure of your chip.

# bashrc
- ssh to your remote machine without running .bashrc `ssh -t ?:.?.?.?  /bin/sh`
- delete all files in directory with a certain extension `find . -name "*.o" -type f -delete`
- use vi as your default editor: edit .bashrc `export VISUAL=vim`  `export EDITOR="$VISUAL"`

# run mpirun on acluster without SLURM  (Hong Kong Cluster (ssh amas@ras2.cse.ust.hk)). You should see all env configurations by:
- add `PermitUserEnvironment yes` to `sudo vi /etc/ssh/sshd_config`
- add all contents of `env` to `vi ~/.ssh/environment`
- restart node daemon `sudo service ssh restart`
- install ahmed module
  - modinfo rack.ko
  - sudo insmod rack.ko enable=1 port=1024
