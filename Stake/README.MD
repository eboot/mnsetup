# Stake Coin Masternode Setup


## Desktop Wallet

1. Open the Stake Coin Wallet Desktop.  
2. Go to RECEIVE and create a New Address: exmaple **MN1**  
3. Send 77777 Stake Coin to new address **MN1**.
4. Wait for 15 confirmations.  
5. Open Debug console **Help -> "Debug Window"** 
6. Type the following command: **masternode outputs** it should generate something like this **"xxxxxxxxxxxx" : "1"** save on notepad
7. Now type in this console **masternode genkey** it will generate the private key of your masternode , write if down somewehere safe

============

# VPS setup

please read code before install
***
```
wget https://github.com/eboot/mnsetup/raw/master/Stake/stake_setup.sh && chmod +x stake_setup.sh && ./stake_setup.sh
```

## Back to Desktop Wallet

8. Go to **Masternodes** tab  
9. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key (masternode genkey)**  
* TxHash: **First value from Step 6 (masternode outputs)**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
10. Click **OK** to add the masternode  
11. Click **Start All**
=======


## Optional if MN is not running
Open Debug console **Help -> "Debug Window" -> masternode start-alias MN1** 

or in vps

copy address MN1 use command **Help -> "Debug Window" -> dumpprivkey your address MN1** save on notepad.
in VPS, use 
**staked importprivkey MN1**
**staked masternode start**
check status
**staked masternode status**

==========

#Note
if wallet in vps error running, like this  **port=33234** bla bla bla bla

```
cd ~
sudo nano .Stake/Stake.conf
```
and remove **port=33234**
