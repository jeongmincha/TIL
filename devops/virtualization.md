## What is Virtualization?

- Use "Computing, Networking, Storage" on a software version of hardware machine
- Hypervisor (HV) → software on the real machine that pulls resources and allocates them to the client
    1. Type 1 (BM)
        - installed directly on top of the host machine
        - most secure, lower latency, most visible in the market
        - VMware ESXi, Microsoft Hyper-V, or opensource KVM
    2. Type 2 (Hosted)
        - there is a host OS layer between HV and the real hardware machine
        - Oracle Virtualbox, Workstation
        - higher latency
- What is VM?
    - software computer.
    - works like a physical computer, includes OS and applications
    - completely independent from the other VMs.
        - → extremely portable
    - HV manage resources allocated from the physical server to the virtual environments
- Key Benefits of Virtualization
    1. Cost savings
        - can run multiple virtual environments on the single infrastructure
        - drastically reduce the physical size of the physical infrastructure
        - save cost for electricity, maintenance
    2. agility and speed
        - when provisioning new environment, it will be easier and faster than making a whole new environment
    3. lower downtime
        - when a host goes out unexpectedly
            - move VMs to another hypervizer