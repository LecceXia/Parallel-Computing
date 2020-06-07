# Parallel-computing

sinfo 查询 slurm 节点和分区信息  
STATE 状态：  
idle 空闲  
mix 使用中，资源不一定全部使用  

sinfo -p partition_name   

srun -p partition_name -w node --pty bash （-p指定分区 -w指定节点）

vim进入代码内部 i进行编辑 编辑完后 esc切换模式 结尾输入:wq 保存并退出编辑


mpicc:not command not found 解决方法  
找到该指令的上一级bin目录 添加到PATH中 即可解决  
export PATH=/...../bin:$PATH  

openMP:  
export OMP_NUM_THREADS=8  
./omp_hello  

MPI:  
  module load openmpi/3.1.2  
  mpirun -np 8 -oversubscribe ./mpi_hello  
