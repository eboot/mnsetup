# Alphanode

Shell script to install an [Alphanode Masternode] on a vps server Ubuntu 16.04. Use it on your own risk. check code before install
***


## Desktop Wallet

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Alphacoin Desktop Wallet.  
2. Go to RECEIVE and create a New Address: exmaple **MN1**  
3. Send 10000 Alphacoin to new address **MN1**.
4. Wait for 6 or 10 confirmations.  
5. Open Debug console **Tools -> "Debug console"** 
6. Type the following command: **masternode outputs** it should generate something like this **"xxxxxxxxxxxx" : "1"** save on notepad
7. Now type in this console **masternode genkey** it will generate the private key of your masternode , write if down somewehere safe
8. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**
=======

## Vps Installation

```
wget https://github.com/eboot/mnsetup/raw/master/Alpha/alpha_setup.sh && chmod +x alpha_setup.sh && ./alpha_setup.sh

```


## Usage

```
alphanode-cli getinfo
alphanode-cli masternode start
```
