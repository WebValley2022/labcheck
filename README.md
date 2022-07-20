# labcheck
Let's get started!


# Environment set up for WebValley2022 on Azure Lab

>## Are you a Windows user?
>### Open Windows PowerShell with Administratory Rights
>
>`# Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0`

## Open a terminal and
## connect to the virtual machine (VM)
`ssh -L 8888:localhost:8888 -p MY_VIRTUAL_MACHINE_PORT wvuser@MY_VIRTUAL_MACHINE_NAME.westeurope.cloudapp.azure.com`

## Activate the conda environment called py38_default
`source ...`

## Start jupyter lab
`jupyter lab --no-browser`

Navigate to http://localhost:8888/lab

# Re-activate conda
```bash
sudo ln -s /anaconda/etc/profile.d/conda.sh /etc/profile.d/conda.sh

echo ". /etc/profile.d/conda.sh" >> ~/.bashrc
echo "conda activate" >> ~/.bashrc

# For those who use zsh
# echo ". /etc/profile.d/conda.sh" >> ~/.zshrc
# echo "conda activate" >> ~/.zshrc

sudo sh -c "echo c.NotebookApp.certfile = u\'\' >> /usr/local/etc/jupyter/jupyter_notebook_config.py"
sudo sh -c "echo c.NotebookApp.keyfile = u\'\' >> /usr/local/etc/jupyter/jupyter_notebook_config.py"

# once logged in
# conda activate py38_default
```


