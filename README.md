# Tutorial 3
This week, we will calculate properties of two-dimensional (2D) materials, graphene and monolayer WTe2, as well as a heterostructure made of these 2D materials.

## Assignment 1

We will start with the DFT calculation of monolayer WTe2. 

### Instructions

1a. Copy the file wte2.scf.in as well as the associated pseudopotentials for both elements to your working directories. This material consists of heavy elements and it is a topological insulator so the spin-orbit interaction is switched on in the input file. You should also use fully relativistic pseudopotentials marked as 'rel' in the names of the files. Open the structure using XCrysDen or the online visualizer. What is the Bravais lattice? Does the structure make sense? Do you understand how the supercell is constructed? Try to display multiple unit cells along the z-direction. What is the distance between the monolayers?

Now, prepare the job script similar to the previously used 'quantum.qsub'. Note that your calculations will be much longer due to the number of electrons and spin-orbit coupling. You will have to adjust your file. You can try first setting time to a few minutes, and check how long each electronic step takes. Estimate your calculation time, change the job script and rerun the calculation.

1b. Based on the knowledge from the last week, prepare and run the band structure calculation. What high-symmetry k-points are relevant for the rectangular Brillouin zone? Does your band structure resemble the one below? What is the difference? Can you think of the possible reason for the discrepancy?

![Test](/images/dos.png)

## Assignment 2

Last week, we have explored the properties of graphite. Now, we will calculate graphene. The typical approach of creating two-dimensional material is to exfoliate the bulk structure. 

### Instructions

2a. Look once again at the WTe2 supercell, and try to create a graphene supercell using the graphite structure from the previous week. Open your file in XCrysden or using the online tool and inspect what you made. Does it make sense? Run the self-consistent field calculation with or without spin-orbit coupling - note that carbon atoms are light so the influence of spin-orbit coupling will be negligible. 

2b. Calculate the band structure along the G-M-K-M direction. How does it differ from graphite? Does it agree with the literature? 
