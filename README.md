EuroSys 2018 Benchmarks
=======================

This repo contains manifests for all of the benchmarks run for the EuroSys 2018 paper
"Scheduling-Context Capabilities: A Principled, Light-Weight OS Mechanism for
Managing Time". 

Manifests
---------

Here we list the manifests and configs for each benchmark.


Benchmark          | Kernel     | Manifest       | Platform | Config                              |
---------          | ---------- |--------        | -------- | ------                              |
Table 1            | MCS        | mcs_micro.xml  | ARM      | sabre_release_O2_defconfig          |
Table 1            | MCS        | mcs_micro.xml  | x64      | x64_release_O2_defconfig            |
Table 1            | Baseline   | base_micro.xml | ARM      | sabre_release_O2_defconfig          |
Table 1            | Baseline   | base_micro.xml | x64      | x64_release_O2_defconfig            |
Figure 6           | MCS        | vm_ipbench.xml | x64      | x64_optiplex9020_udpecho_defconfig  |
Table 2            | Baseline   | base_rump.xml  | x64      | notrt-redis-rumprun-x86_64_defconfig|*
Table 2            | BMK        | rump.xml       | x64      | make hw_redis_x64                   |*
Figure 7/Table 2   | MCS        | mcs_rump.xml   | x64      | rt-redis-rumprun-x86_64_defconfig   |
Table 3/Figure 8   | MCS        | mcs_micro.xml  | ARM      | sabre_aes_defconfig                 |
Table 3/Figure 8   | MCS        | mcs_micro.xml  | x64      | x64_aes_defconfig                   |
Figure 9           | MCS        | mcs_micro.xml  | ARM      | sabre_smp_release_O2_defconfig      |
Figure 9           | Baseline   | mcs_micro.xml  | x64      | x64_smp_release_O2_defconfig        |
Figure 10          | MCS        | mcs_micro.xml  | ARM      | sabre_criticality_defconfig         |
Figure 10          | MCS        | mcs_micro.xml  | x64      | x64_critcality_defconfig            |
Table 4            | MCS        | mode_switch.xml| x64      | crit_k_defconfig & crit_ul_deconfig |*
Figure 11          | MCS        | mcs_micro.xml  | ARM      | sabre_ulscheduler_defconfig         |
Figure 11          | MCS        | mcs_micro.xml  | x64      | x64_ulscheduler_defconfig           |

### Getting the code

    repo init -u https://github.com/pingerino/eurosys18.git -m <MANIFEST>.xml

### Building the code

    make <CONFIG>
    make -j

### Running the code

    Please see the seL4 documentation for running on hardware.

Other software
--------------

 * LITMUS/Linux version: 4.9.20-litmus
 * NetBSD: 7.0.2
 * Redis Version: 3.0.6
 * YCSB: 0.1.4


