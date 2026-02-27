# RFD3 simple enzyme design

Steps:  
1. Activate the conda environment (if you have installed RFD3 in one)  
<code>conda activate RFD3_foundry</code>  
2. Make folder for input files and download them  
<code>mkdir input_pdbs  
wget https://raw.githubusercontent.com/RosettaCommons/foundry/production/models/rfd3/docs/enzyme_design.json  
wget -P input_pdbs https://raw.githubusercontent.com/RosettaCommons/foundry/production/models/rfd3/docs/input_pdbs/M0255_1mg5.pdb</code>
3. Run motif scaffolding with the following command  
<code>rfd3 design out_dir=output inputs=inputs</code>