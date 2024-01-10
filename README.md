# SLoMo
This repo contains some instructions associated with the paper "SLoMo: A General System for Legged Robot Motion Imitation from Casual Videos". 

[link](https://ieeexplore.ieee.org/abstract/document/10246373), [arXiv](https://arxiv.org/pdf/2304.14389.pdf)


## reconstruction
For reconstruction, we use [PPR](https://gengshan-y.github.io/ppr/), a physics-informed reconstruction method. Please refer to the [instructions](https://github.com/gengshan-y/ppr) for more details. For general monocular reconstruction, please checkout [Lab4d](https://lab4d-org.github.io/lab4d/). 

We provided some of the trajectories generated from the reconstruction process in the `data` folder.

## offline policy optimization
To optimization an policy/reference trajectory offline, we use examples provided from [ContactImplicitMPC.jl](https://github.com/dojo-sim/ContactImplicitMPC.jl) to solve a contact-implicit trajectory optimization problem or optimize an imitation-learning policy using the [motion_imitation repo](https://github.com/erwincoumans/motion_imitation).

## online control
To control the robot online, we use [CI-MPC](https://github.com/dojo-sim/ContactImplicitMPC.jl) to track offline trajectories. One can also inference the network trained from imitation learning to generate controls on quadrupeds.

## citation
If you find our work useful, please consider citing our paper:
```
@inproceeding{zhang_slomo_2023,
        title = {SLoMo: A General System for Legged Robot Motion Imitation from Casual Videos},
        url = {https://ieeexplore.ieee.org/abstract/document/10246373},
        author = {Zhang, John Z and Yang, Shuo and Yang, Gengshan and Bishop, Arun L and Ramanan, Deva and Manchester, Zachary},
        journal = {IEEE Robotics and Automation Letters},
        year = {2023}
}
```
