

daemon are like windows services for linux

We can see them using:

`ps -A`

`top` Can be used to see the system resources utilization


`systemctl` can be used to interact with daemons (stop, start, jobs, ect)

`ps fax | more` can display child processes, it will be displayed as:

[parent process]
	\_ child process
	
Killing a parent process will kill its child processes

`pstree` allows us to see the tree of processes