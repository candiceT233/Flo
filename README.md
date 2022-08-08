# Flo
Parallel network flows using OpenMP and CUDA.
Project website at https://joshkorn.com/flows.html

# Algorithm Options
- FlowPushRelabel: seq, cpu, gpu (default)
- FlowDinic: seq, cpu (default)
- FlowEdmondsKarp: seq, cpu (default)

# Test Environment
- OS: Ubuntu 20.04, CUDA 11
- Chameleon Node ID: nc29
- Node Spec: https://chameleoncloud.org/hardware/node/sites/uc/clusters/chameleon/nodes/3993facb-7a19-4847-adeb-30eca59aebfa/
- Additional dependency: sudo apt-get install freeglut3 freeglut3-dev

# Test Results
- Time in seconds, tested with 3 trials.
## Edge density: 0.01
### graph 0, 100 vertices, 49 edges
Avg time of edKarpCPU: 0.0824739 \
Avg time of dinicCPU: 0.000914972 \
Avg time of pushRelabelLockFree: 0.00202809 \
Avg time of pushRelabelLockFreeGPU: 0.378128
### graph 1, 400 vertices, 798 edges
Avg time of edKarpCPU: 0.00186914 \
Avg time of dinicCPU: 0.00927935 \
Avg time of pushRelabelLockFree: 0.0248464 \
Avg time of pushRelabelLockFreeGPU: 0.335422
### graph 0, 10000 vertices, 499950 edges
Avg time of edKarpCPU: 0.290168 \
Avg time of dinicCPU: 0.277439 \
Avg time of pushRelabelLockFree: 0.519422
## Edge density 0.002
### graph 0, 10000 vertices, 99990 edges
Avg time of edKarpCPU: 0.180829 \
Avg time of dinicCPU: 0.278054 \
Avg time of pushRelabelLockFree: 0.356453
### graph 1, 40000 vertices, 1599960 edges
Avg time of edKarpCPU: 3.04375 \
Avg time of dinicCPU: 4.35346 \
Avg time of pushRelabelLockFree: 7.15754
## Edge density 0.008
### graph 0, 10000 vertices, 399960 edges
Avg time of edKarpCPU: 0.226493 \
Avg time of dinicCPU: 0.237139 \
Avg time of pushRelabelLockFree: 0.508934
### graph 1, 40000 vertices, 6399840 edges
Avg time of edKarpCPU: 12.373 \
Avg time of dinicCPU: 4.22206 \
Avg time of pushRelabelLockFree: 9.20795