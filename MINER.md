# WebGenie: Miner documentation

### Testing
We recommend testing your miner on Testnet (SN 214) before deploying to mainnet

### Prerequisites
- Python 3.12 or higher
- A Bittensor wallet with TAO
- Access to the Bittensor network

### Environment Setup
Install pm2:
```bash
npm install pm2 -g
```

Clone the repository:
```bash
git clone https://github.com/web-genie-ai/web-genie-ai.git
cd web-genie-ai
```

Create virtual environment:
```bash
# Create virtual environment
conda create -name venv python=3.12
```
```bash
# Activate virtual environment
conda activate venv
```
Miner Registration:
```bash
btcli subnet register --netuid __   # Use 214 for testnet
```

### Running the miner

Install  dependencies:
```bash
pip install -r requirements.txt
```
Start the miner:
```bash
pm2 start neurons/miners/miner.py --name "webgenie_miner" --interpreter python -- --netuid [NET_UID] --subtensor.network [finney | test] --wallet.name [coldkey_name] --wallet.hotkey [hotkey_name] --logging.debug --axon.port [axon_port]
```




