# Water-Kaolinite-LAMMPS
This project contains the LAMMPS simulation data generated from MSI2LMP to simulate 17k ppm CsCl between Kaolinite layer using ClayFF force field. The result files are in post directory. The force field can be obtained from MSI2LMP repository on LAMMPS github. This force field is outdated but it works fine with the MSI2LMP, format wise.

This is an unfinished work. The simulation is still broken, since there are bond and angle lost due to transfer from water simulation to kaolinite layer. Therefore, this work should not be used for real cases. 

## How to Use:

1. Create Water model created with material studio and export to msi/car
2. Make sure all atoms are labeled according to the ClayFF.frc
3. Convert Water model to LMP data with MSI2LMP and ClayFF.frc
4. Simulate Water using Lammps
5. Create Kaolinite layer in material studio with existing Water mode
6. Redo step 1 to 3 with Water+Kaolinite model 
7. Use the .xlsx to convert the Water simulation result data and append it to the LMP data of Kaolinite layer (see example: Double-Kaolinite_4x4x2_W-opt.data, Double-Kaolinite_4x4x2_W.data and Water_CsCl_1M.data)
8. Run Lammps
