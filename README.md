# Vitality 
hell script to install a [Vitality Masternode](http://vitality-coin.com/) on a Linux server running Ubuntu 16.04.  
This script will install **vitality v1.0**.

***
## Vultr VPS Recommended
[Believe Me, I have Tried Everything. Click Here for Vultr](https://www.vultr.com/?ref=7410771)
***
## Installation:
```
wget -q https://raw.githubusercontent.com/Chased1k/vitality/master/vitality_install.sh
bash vitality_install.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the vitality Core Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **10000** **POSQ** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  ** Tools -> "Open Masternode Configuration File"
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6** 
* Output index:  **Second value from Step 6** It can be **0** or **1**
9. Click OK and exit the Wallet.
10. Open vitality Core Wallet, go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again.
10. Click **Start All** or **Start Alias**
11. If you are not able to see your **Masternode**, try to close and open your desktop wallet.
***

## Usage:
```
vitalityd getinfo
vitalityd masternode status
vitalityd mnsync status
```
Also, if you want to check/start/stop **vitality** , run one of the following commands as **root**:
```
systemctl status vitalityd #To check the service is running.
systemctl start vitalityd #To start vitality service.
systemctl stop vitalityd #To stop vitality service.
systemctl is-enabled vitalityd #To check whetether vitality service is enabled on boot or not.
```


## Donations:  

Any donation is highly appreciated.  

**VIT**: VDwKwAWwVdYuYLRo6y92xyVckJ3GsF7aZQ 
**BCH**: qzgsarlyahpdemyapkm0mlurwwnmjsjznvmxm85e4y  
**ETH**: 0xA78901Aed64d92360917222d7dC2697a4AD0D608  
**LTC**: LYx9AEcYLh2xyz1G4ER4tQCw24FyXfbdC6  
