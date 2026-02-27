# RFD3 installation process (easy install)

Steps:  
1. create conda environment  
<code>conda create -n RFD3_foundry python=3.12 -y</code>
2. Activate the conda environment  
<code>conda activate RFD3_foundry</code>
3. Install RFD3 via pip  
<code>pip install "rc-foundry[rfd3]"</code>  
Pitfall: If zsh is used as terminal shell, quotes are required to escape the rectangular brackets  

# Test installation  
Steps:
1. Download input files  
<code>mkdir input_pdbs  
wget https://raw.githubusercontent.com/RosettaCommons/foundry/production/models/rfd3/docs/demo.json  
wget -P input_pdbs https://raw.githubusercontent.com/RosettaCommons/foundry/production/models/rfd3/docs/input_pdbs/M0255_1mg5.pdb  
wget -P input_pdbs https://raw.githubusercontent.com/RosettaCommons/foundry/production/models/rfd3/docs/input_pdbs/7v11.pdb  
wget -P input_pdbs https://raw.githubusercontent.com/RosettaCommons/foundry/production/models/rfd3/docs/input_pdbs/1bna.pdb</code>
2. Run demo example  
<code>rfd3 out_dir=demo_output inputs=demo.json</code>  

# Pitfalls
Pitfall:  
Make sure you are still in the conda environment
If run fails on gpu because of a too modern gpu, install  
<code>pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu128 --upgrade --force-reinstall</code>
