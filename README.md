<h2 align=center>Create octra wallet using CLI</h2>

![Watch the video](https://i.ytimg.com/vi/bJhVfrvdxVA/maxresdefault.jpg)

## 💻 Installation
- Open any Linux based terminal, you can use VPS / WSL (On windows) or simply you can use virtual IDE as well
- If you don't have any VPS or not have WSL installed in your Windows, then simply go for virtual IDE
- One virtual IDE, I use the most is [Github Codespaces](https://github.com/codespaces), visit this link and choose a blank template
> [!NOTE]
> If you already have 2 templates opened in github codespace, in that case you need to delete one before opening another one
- Now install `curl` command first
```
command -v curl >/dev/null 2>&1 || { sudo apt-get update && sudo apt-get install -y curl; }
```
- Now use the below command to generate your octra wallet
```
curl -sSL https://raw.githubusercontent.com/darkcandy-off/octra-wallet-cli/refs/heads/main/start.sh -o start.sh && chmod +x start.sh && ./start.sh
```
 ## ⚡ Post-Installation
 - Visit [octra faucet](https://faucet.octra.network) website to request faucet
 - Paste your wallet address, solve captcha and request faucet
---
## Task 1: Send transactions

**1. Install Python**
```bash
sudo apt install python3 python3-pip python3-venv python3-dev -y
```
**For termux users**
```bash
pkg install python3 python3-pip python3-venv python3-dev -y
```

**2. Install CLI**
```bash
git clone https://github.com/octra-labs/octra_pre_client.git
cd octra_pre_client

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

cp wallet.json.example wallet.json
```

**2. Add wallet to CLI**
```bash
nano wallet.json
```
**Termux must install Nano**
```bash
pkg intall nano
```

* Replace following values:
  * `private-key-here`: Privatekey with `B64` format
  * `octxxxxxxxx...`: Octra address starting with `oct...`


**3. Start CLI**
```bash
python3 -m venv venv
source venv/bin/activate
python3 cli.py
```
* This should open a Testnet UI

![image](https://github.com/user-attachments/assets/0ba1d536-4048-4899-a977-4517b2e522cd)


**4. Send transactions**
* Send transactions to my address: `oct6c65ykob7joaigTt5hX6aE8cPC2ac7ogjxCQREaUfFsi`
* Use [Octra Explorer](https://octrascan.io/) to find more octra addresses


**5. Use Alternative Script**
* If you have issue with official script, I just refined the script with optimizated UI, you can replace the current one with mine by executing this command:
```bash
curl -o cli.py https://raw.githubusercontent.com/darkcandy-off/octra-wallet-cli/refs/heads/main/cli.py
```
**For next day cmds**
```bash
cd octra_pre_client
source venv/bin/activate
python3 cli.py
```

**6. Share Feedback**

Always share your feedback about the week's task in discord

---

## Wait for next steps
Stay tuned.
