
No. Process:                        Mean time (average of 3 runs)           Parallel speed-up, S:
===========                         ============================:           ====================
1                                   0.01374597                              1.0
2 (same node)                       0.00807676                              1.701916363
4 (same node)                       0.00540655                              2.542466083
4 (2 nodes, 2 per node)             0.017363433                             0.791661994
8 (2 nodes, 4 per node)             0.173911                                0.079040256
12 (3 nodes, 4 per node)            0.226707                                0.060633196


Architecture that the timing runs were performed on: 
DEC-10 machines.


A brief interpretation of these results:
As the number of nodes reaches a certain point, the application takes longer to compute than in serial because the overheads of collecting the nodes from other machines and then sending and recieving the values to one another via collective communication takes more time than running in serial. On the same node the speed increased as there was no latency. With increasing number of nodes the latency comes into affect when the nodes are sending information to another, hence the increased value of the parallel speed up. The lower this value the added value of running in parallel.

