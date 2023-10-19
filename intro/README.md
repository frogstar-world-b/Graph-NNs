## Notes about creating a conda environment to run notebook
Run the following commands in terminal:

`conda create -n gnn_py9 python=3.9>> conda activate gnn_py9`

`pip install torch torchvision torchaudio`

`pip install --verbose --no-cache-dir torch-scatter`

`pip install --verbose --no-cache-dir torch-sparse`

`pip install --verbose --no-cache-dir torch-cluster`

`pip install torch-geometric`

`conda activate gnn_py9`



If you need to track runs with ngrok, go to https://ngrok.com/download

`brew install ngrok/ngrok/ngrok`

Download ZIP File, which is found here: https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-darwin-amd64.zip

`sudo unzip ~/Downloads/ngrok-v3-stable-darwin-amd64.zip -d /usr/local/bin`
