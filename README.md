
# Contest is over, now the real work begins. New version upcoming including all drivers and miner details. 


# A blockchain without boundaries.

The following instructions will walk you through the process of setting up a portable Burstcoin node. This device is fully
capable of running a node, a miner, as well as hosting a shared or tethered network. This could be critical to use as we
have demonstrated with the Proof of Life.

Proof of Life: https://medium.com/@nixops_56291/proof-of-life-resurrecting-technology-653167c5763a


All features of the drive shipped by Western Digital still work with and after this installation. Even the mobile app works
as well as desktop apps. This is only adding a burst node to the functionality of the device, which could be extended to add
more features needed.

# Requirements
1. WD MyPassport Wireless Pro: https://www.wdc.com/products/portable-storage/my-passport-wireless-pro.html
2. An ssh client. (literally ssh)
3. A device that you can connect to the drive's network to verify it is working.
4. Patience, syncing from genesis block can take some time.
5. Download the burst wallet: https://github.com/PoC-Consortium/burstcoin/releases/



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

10. Copy the configs/brs-default.properties file over to your burstcoin directory/conf. (modify it if you want, but default is h2)

Restart the WD Wireless Pro.

# Accessing the node.

Inside the 192.168.60.1 default settings you can change what wifi you are accessing and broadcasting. This is important
as this can allow you to tether the device to mobile and or other sources. To access the Burst node, you can then navigate
to either of the following URLS:

MyPassport.local:8125

192.168.60.1:8125


# Radio Peer

Please use the following host if you are demoing via radio: useburst.com(non encrypted) as your peer. This is important as if you use it
it is non ssl and is only there as accessible per requirements of the project. Please be aware of any and all radio operator
laws in your country/region. We are not responsible for any legal action you may or may not encounter if you do not adhere to 
those laws.


# Mounting a radio as a modem
This device ships with a fully functioning linux operating system, you can mount any device that would be used on a desktop
or laptop on this device. This also goes for a variety of networking options. There is a lot to be explored. At this time
we are working to 100% simplify this, once done it will be updated here to reflect that. But for the impatient, you can do
some digging and find what you need for this.

# Extending functionality
You can connect this to any device that is supported or can be supported by Linux. This is important as it could allow you 
to get very creative on use of either a radio and or some other SDR projects. You can also use a handheld amateur radio 
as a modem in order to transmit, YOU MUST BE LICENSED. This drive can be powered by solar or crank power under extreme 
duress. The goal of this project was to demonstrate you could do this anywhere and anytime, if you had to.

# Tools
The following are a list of tools that you could run on another device to connect to the drive. These tools further the 
uses of the drive and deployment options.

Burst Messaging:
Built into the wallet, so anyone with access to a browser can access the messaging service on chain in the wallet.

CloudBurst : https://github.com/CurbShifter/CloudBurstDAPP
CloudBurst can be used to upload documents, immutably to the chain. This is not an ipfs hack, a real on chain storage.

BurstCoupon: https://github.com/CurbShifter/BurstCoupon
BurstCoupon can be used to distribute coins in a voucher model that can be claimed through a browser.

PChains: http://burst-marketplace.binary-dev.com/pchains/documentations/doc.php
Service built on chain to provide private blockchains using the Burst Messaging.



# TODO
1. Adding miner instructions, this was dropped as in a case of extreme scenarios we may need to just transmit various communications
of life. (this is working now, but needs to be simplified). 
2. One button install, at this time about 85% reliable. Still addressing issues
3. Adding a wallet icon and link into the admin console.
4. Provide build root instructions for cross compiling.
5. GPG support is being added and rust. 

# Notes
More of the toolchains and cross compiling steps are being added. The toolkits and all are files and things I used to go 
through several iterations of this device. Some features are being worked on for future simplified setup as well as
configurations.


# Factory Reset

If you factory reset, you will only need to setup the S99 script as the rest is still in the default stored directories you have
used. If you do encounter issues, just factory reset a few times and it will actually recover.

If you have questions or comments, ask away.

