# VALIDATED-VIV
In this repository, a validated case of two-degree-of-freedom vortex-induced vibrations at Reynolds number of 100 and reduced velocity $U^*$ of 6 is presented for OpenFOAM 2206. I tested the case and in its current condition, it should work on OF2206. The reference paper used for validation is given below. 

I did not find acceptable results using a variable time-step, so I recommend a fixed time-step. I prefer rigidBodyMotion solver over sixDoFRigidBodyMotion solver. Also, it is important to take the effects of added mass into condieration when calcualting sprung mass. The added mass effects are not used in finding the spring stiffness using natural frequency formula. 

In the reference below dimensional natural frequency of the system is fixed at $f_N = 0.166$ for all the Reynolds numbers and all the reduced velocities. However, the non-dimensional natural frequency $F_N$ differs in each case. Also, the non-dimensioanl mass $m^*$ is 10 and structural damping ratio $\zeta$ is zero for all the cases. The mesh has around 50k cells and is two-dimensional (actually three-dimensional with a unit span). To get the cylinder's trajectory, run ./makeFiles in a Linux shell environment. 

Reference:
Prasanth, T.K., Mittal, S., 2008. Vortex-induced vibrations of a circular cylinder at low Reynolds numbers. J Fluid Mech 594, 463–491. https://doi.org/10.1017/S0022112007009202
