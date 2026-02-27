# RFD3 installation process (from source)

Steps:  
1. create conda environment  
<code>conda create -n RFD3_foundry_from_source python=3.12 -y</code>
2. Activate the conda environment  
<code>conda activate RFD3_foundry_from_source</code>
3. Download github repository  
<code>git clone https://github.com/RosettaCommons/foundry.git</code>
4. Install RFD3 via pip  
<code>cd foundry  
pip install -e ".[rfd3]"</code>  
Pitfall: If zsh is used as terminal shell, quotes are required to escape the rectangular brackets  
5. Download model weights (checkpoint file)  
<code>cd models/rfd3/  
mkdir checkpoints  
foundry install rfd3 --checkpoint-dir ./checkpoints</code>   


# Test installation  
Steps:
1. Run demo example  
<code>cd docs</code>  
<code>rfd3 out_dir=demo_output inputs=demo.json</code>  
Pitfall: Make sure you are still in the conda environment

