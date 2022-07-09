## High-Performance Linpack Optimization Mini-Challenge

This challenge description is directly quoted from the DUSCC `#general` slack channel:


### Challenge

Goal: Maximize Gflops achieved by the High-Performance Linpack (HPL) Benchmark on Hamilton 7/8.

Instructions:

1. Follow the steps provided at https://github.com/DUSCC/wiki/blob/main/pages/LINPACK.md to build and run a basic version of HPL.
2. For all runs, please make sure that each of your test cases runs at least a minute (walltime) to ensure stable timing measurements since Linpack does not do averaging (as can be seen in testing/ptest/HPL_pdtest.c on lines 197 ff.). To achieve this, please choose sufficiently large matrix sizes, with "sufficiently large" being dependent on the number of MPI ranks available.
4. Tune the parameters in the HPL.dat file and play around with different MPI libraries, BLAS libraries, compilers and compiler flags to maximize the number of Gflops that Linpack reaches.
5. Plot your measurements, e.g. with gnuplot, for comparison.
6. Ensure that your results are reproducible, e.g. by providing build and run scripts.
Limitations:
1. Do not use more than 2 nodes of Hamilton 7/8.
2. Do not execute runs longer than 2 hours.

Hints:

1. For a start, you might want to use a HPL.dat file generated from system parameters, e.g. via https://www.advancedclustering.com/act_kb/tune-hpl-dat-file/
2. Main parameters relevant for tuning: problem size N, block size NB, grid configuration P x Q = MPI Ranks
3. For time measurements, use nodes with exclusive access. Please be aware that Hamilton 8 is currently rather busy and jobs might take days to be scheduled if exclusive access via the "multi" queue is required. You might want to consider using Hamilton 7 instead.
4. Use "module avail" to see which compilers, MPI libraries, and BLAS libraries are already available on Hamilton 7/8 via "module load". Feel free to compile and use architecture specific libraries as you see fit.
5. In case you need to work interactively, use the cmd line tool "screen" to recover from unintended disconnects


### Deadline

Deadline for the challenge is our meeting in the week of the 18th of July.
