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

Now, we will perform density of states (DOS) calculations for the bulk silicon. 

### Instructions

2a. Copy the files ‘Si.nscf.in’ and ‘Si.dos.in’ to the directory containing calculations with the optimized lattice constant. Make sure that celldm(1) in these files is equal to the optimized lattice constant. Run the non-self-consistent calculation using the file ‘Si.nscf.in’. Note that the k-mesh is much larger than in the previous runs and a longer time will be required to finish the calculation. When the calculation is terminated successfully, run the file ‘Si.dos.in’ using the script 'dos.sh'. 

2b. The result will be written in a file ‘Si.dos.dat’ containing three columns and the value of Fermi energy at the beginning of the file. Plot energy vs dos(E) using your favorite plotting tool, for example, Gnuplot, Python, or if you really want, in Excel. Don’t forget to shift the Fermi energy printed at the beginning of the file. For example, type ‘module load gnuplot’, then ‘gnuplot’ and then use the command:
plot 'Si.dos.dat' using ($1-<Fermi_energy>):2 with lines

Compare the result with the plot below. Does it agree? Based on the calculated DOS, would you classify crystalline Si as an insulator, a semiconductor, or a metal?

![Test](/images/dos.png)
