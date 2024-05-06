# ops
**Title:** A Two-step Nonlinear Factor Sparsification for Scalable Long-term SLAM Backend

**Venue:** ICRA'24

**Authors:** Binqian Jiang and Shaojie Shen from the [HKUST Aerial Robotics Group](https://uav.hkust.edu.hk/).

## Abstract
This paper proposes a new nonlinear factor sparsification paradigm for general feature-based long-term SLAM backend. 
Given a pose sparsification policy, we aim to scale the SLAM problem with space explored instead of time in a principled way so that the number of time-indexed poses can be limited. At the same time, their influence and the long-lived landmarks are appropriately maintained. To do this, we propose a new two-step sparsification pipeline. 
Given a pose node to remove, the first step is performed in the Markov blankets of affected landmarks. It transforms pose-landmark constraints into pose-pose constraints while preserving observability and minimizing information loss in the blanket. Moreover, since landmarks are conditionally independent, we can do this in parallel, disconnecting a pose from all the landmarks. 
The second step marginalizes the pose of interest with pure pose-wise constraints without affecting landmarks. Our method decouples the management of landmarks from pose-only measurements, making it general for any feature-based SLAM. We also give a practical example of how our backend works by concatenating it to a monocular VIO frontend. In simulation and real-world dataset, our sparsified backend is accurate and efficient. We open-source our backend, along with the VIO+Backend example, to contribute to the community's betterment.
