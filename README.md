# OCTRA-terminal
**a terminal wallet reminiscent of dos-era tui interfaces — but built with modern asynchronous architecture**
# what it does
shows your octra wallet balance and tx history
lets you send one or many transactions
exports your private key or full wallet file
# works on
- linux
- mac
- windows (some features like clipboard may not work)
# what you need
- python 3.8 or higher
- internet connection
- your wallet file (private key)
# how to install and run (step by step)
**first of all you need install and update some packages**
1. **Update server packages**
```console
sudo apt-get update && sudo apt-get upgrade -y
```

2. **Main Packages**
```console
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev ca-certificates  -y
```

3. **Python3, pip**
- **here we install python**
```console
## Python 3.8 Pip, Python3 Install
sudo apt install -y python3-pip
sudo apt install pip
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
```
# install the client
```bash
git clone https://github.com/octra-labs/octra_pre_client.git
cd octra_pre_client
python3 -m venv venv
source venv/bin/activate # for windows use: venv\Scripts\activate
pip install -r requirements.txt
cp wallet.json.example wallet.json
```
now open wallet.json and edit it (change placeholders to your wallet data):
```bash
{
  "priv": "private-key-here",
  "addr": "octxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "rpc": "https://octra.network"
}
```
**RUN**
```bash
./run.sh       # on linux/mac
run.bat        # on windows
```
