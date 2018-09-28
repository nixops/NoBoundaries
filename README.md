# A blockchain without boundaries.

The following instructions will walk you through the process of setting up a portable Burstcoin node. This node is fully
capable of running a node, a miner, as well as hosting a shared or tethered network. This could be critical to use as we
have demonstrated with the Proof of Life.

Proof of Life: https://medium.com/@nixops_56291/proof-of-life-resurrecting-technology-653167c5763a


# Requirements
1. WD MyPassport Wireless Pro
2. An ssh client.
3. A device that you can connect to the drive's network to verify it is working.
4. Patience, syncing from genesis block can take some time.
5. Download the burst wallet: https://github.com/PoC-Consortium/burstcoin/releases/download/2.2.3/burstcoin-2.2.3.zip



# How-to:

1. Make sure that the drive is reset to stock, you can do this by turning it on and holding the power and wps button at 
same time for 10 seconds to accomplish this.

2. Next, connect to the WD MyPassport Wireless Pro's wifi network, the password for default was on a sticker or the last
eight alpha numeric characters in the serial number printed on the bottom.

3. Once connected you will need to go to the following URL: 192.168.60.1 (Keep in mind you can use MyPassport.local as well)

4. Once there, navigate to the admin tab and enable ssh, add a password here.

5. Now from your laptop/desktop please execute the following command: ssh root@192.168.60.1 and use the defined password.

6. Once you are logged in, you will now need to move some files to a location on the drive. So first lets navigate to the 
Passport storage drive. In here create a folder, any name you choose. Do note the name you choose will need to be updated
in the S99 script.

7. Once there, copy and uncompress the burst wallet as well as the JDK. 

8. While still logged into the shell you will need to copy over the scripts/S99Burst script. You will need to copy it into
/etc/init.d/ directory on the drive. You may need to adjust the S99 accordingly to your locations and paths.

9. You can now exit the shell.

10. Copy the configs/brs-default.properties file over to your burstcoin directory/conf. 

Restart the WD Wireless Pro.



# Accessing the node.

Inside the 192.168.60.1 default settings you can change what wifi you are accessing and broadcasting. This is important
as this can allow you to tether the device to mobile and or other sources. To access the Burst node, you can then navigate
to either of the following URLS:

MyPassport.local:8125
192.168.60.1:8125


# Extending functionality
You can connect this to any device that is supported or can be supported by Linux. This is important as it could allow you 
to get very creative on use of either a radio and or some other SDR projects. You can also use a handheld amateur radio 
as a modem in order to transmit, YOU MUST BE LICENSED. This drive can be powered by solar or crank power under extreme 
duress. The goal of this project was to demonstrate you could do this anywhere and anytime, if you had to.


# TODO
1. Adding miner instructions, this was dropped as in a case of extreme scenarios we may need to just transmit various confirmations
of life. (this is working now, but needs to be simplified).
2. One button install, at this time about 75% reliable. Still addressing issues
3. Adding a functional piece to the UI to ease use of the wallet.

