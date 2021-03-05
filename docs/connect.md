---
id: connect
title: Connect to DAppNode
---

## Via VPN

For connecting to DAppNode 0.2.0 OpenVPN, you will need to have a client that supports the OpenVPN protocol in every device with which you´d like to connect to your DAppNode. Also note that if you are running DAppNode in a physical server with WIFI you can connect to your DAppNode without need of the VPN, just by connecting to the DAppNode WIFI.

Once you have your DAppNode running, you will get an URL in your terminal from where you can download the OVPN config file and open it in your device with your OpenVPN client.

If you have still not installed your OpenVPN client . Just download the credentials file and follow the instructions.

Opening this OVPN file will configure your VPN connection to your DAppNode from your device. The first device VPN connection will have super admin privileges so you can access and manage the DAppNode admin UI; this user cannot be deleted.

Take into account that some VPN clients might send all traffic through the VPN, which is not very ideal if you have many people connected to your DAppNode, or only to send traffic which points to an ETH domain.

DAppNode is not intended to manage all the traffic of the devices connected to it, only the ETH domains access requests.

<!-- prettier-ignore-start -->
!!! info
    When you download and install a VPN credentials file, only your ETH traffic will be going out through the VPN, the regular IP traffic will still be done with your regular IP. If you want to route all your Internet traffic through your DAppNode so you are behind your VPN, you should configure it in your VPN client settings by checking the Box "Send all traffic".
<!-- prettier-ignore-end -->

These are the recommended Open VPN clients for each OS:

- Mac os: [Tunnelblick](https://tunnelblick.net/)
- Ios: [Open VPN connect](https://itunes.apple.com/us/app/openvpn-connect/id590379981)
- Windows: [Open VPN (community installer)](https://openvpn.net/community-downloads/)
- Android: [Open VPN for Android](https://play.google.com/store/apps/details?id=de.blinkt.openvpn)
- Linux: Already included in recent versions.

Depending on your OS these are the instructions for installing our recommended OpenVPN clients.

<!-- prettier-ignore-start -->
!!! info
    Please note that for the ovpn to be correctly downloaded from the link given you will need to have the TCP port 8092 opened and that the default port to connect via OpenVPN is 1194 UDP. UPnP should have opened them for you if your router has UPnp enabled, if not you will have to open them manually
<!-- prettier-ignore-end -->

## Linux

### Ubuntu / NetworkManager

OpenVPN comes installed in Ubuntu recent versions, but to be sure, follow these steps. Run the terminal application:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ubuntu1.png">


Install OpenVPN and plugin for NetworkManager:

    sudo apt-get install network-manager-openvpn-gnome openvpn

Once the installation is complete, restart Network Manager by typing:

    sudo service network-manager restart

Go to "Settings -> Network" and click to the "" button to add a VPN connection:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ubuntu2.png">


Select "Import from file..."

 
  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ubuntu4.png">


Browse the filesystem to select the downloaded file:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ubuntu3.png">


Add the profile with the default settings:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ubuntu5.png">


Now you can connect selecting the profile from the network tray icon:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ubuntu6.png">


## MacOS

The recommended OpenVPN client is Tunnelblick and you can download it [here](https://tunnelblick.net)


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/mac1.png">


Once you have followed the steps to install the tunnelblick client in your MAC, download the file from the URL given in the console to download the OVPN file with your credentials.

If you have already downloaded the config file before installing Tunnelblick, you can select the "I have a config file" option and browse to its location. If not, once you have downloaded the OVPN file, just double click on it and Tunnelblick will add the config for you.

Select your preferred option about the users that will have access to the config.


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/mac4.png">


The system will probably ask for your admin password to install the VPN configuration, and it is done!


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/mac5.png">


Just open Tunnelblick in your MAC and click on Connect DAppNode.


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/mac6.png">


Once connected you can already access http://my.admin.dnp.dappnode.eth with your new OpenVPN connection!


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/mac8.png">


## iOS

The recommended OpenVPN client is OpenVPN Connect and you can download it [here](https://itunes.apple.com/us/app/openvpn-connect/id590379981?mt=8)


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ios1.png">


Once you have installed it you can just scan the QR code and hit download:


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ios4.png">


and click in "Open in OpenVPN"


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ios5.png">


Tap the add button and name your connection


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ios7.png">


The phone will ask you permission for OpenVPN to add a configuration profile , please do.

And it is done, you can just connect to your new OpenVPN now


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ios9.png">
 
  
After a few seconds, you will see in the OpenVPN interface that you are connected. You can either connect to your server through the OpenVPN app or directly from the phone´s "VPN" menu in "Settings"


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/ios10.png">


Once connected you can access http://my.admin.dnp.dappnode.eth with your new OpenVPN connection!

## Android

Install **OpenVPN for Android** from [Google Play](https://play.google.com/store/apps/details?id=de.blinkt.openvpn) or [F-Droid](https://f-droid.org/en/packages/de.blinkt.openvpn/):


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android1.jpg">


Download the OpenVPN profile from the URL or scanned QR code:


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android2.jpg">


Open the downloaded file and import it to the application, then save it with your preferred name:


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android3.jpg">


Select the saved profile to connect to it:


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android4.jpg">


Accept the connection request:


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android5.jpg">


You should see a connection log similar to this:


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android6.jpg">


Once connected, you should be able to browse the DAppNode Admin page:

[http://my.admin.dnp.dappnode.eth](http://my.admin.dnp.dappnode.eth)


  <img width="300" src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/android7.jpg">


## Windows

Download the recommended client for [OpenVPN WINDOWS INSTALLER (NSIS)](https://openvpn.net/community-downloads/) and follow the steps to install it:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows1.png">



  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows2.png">



  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows3.png">


Download the file from the provided link by the DAppNode administrator.


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows4.png">


Run the OpenVPN GUI program:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows5.png">


Select "Import file..." from the tray bar icon (right click):


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows6.png">


Select the downloaded file:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows7.png">


Finally, select "Connect" from the tray bar icon menu:


  <img src="https://github.com/dappnode/DAppNode/raw/master/doc/openvpn/windows8.png">


## Via WIFI

### Connect to DAppNode via the built-in Wifi hotspot

If you have your DAppNode installed in a physical device with Wi-Fi, you can directly connect to your server's Admin UI by connecting your client device to the DAppNode's wifi hotspot.

When you connect your DAppNode server to your router via Ethernet you will see a network called DAppNodeWIFI, just connect to that Wifi using the defaul password "dappnode" and you will have direct access to your DappNode server ADMIN UI while connected to that WIFI.

<!-- prettier-ignore-start -->

!!! warning

Please immediately change the name of the WIFI and the password by setting up the new values in the WIFI package under the system tab.

<!-- prettier-ignore-end -->


  <img src="../images/wifipasswordssid.png">


Once you have entered the admin UI you can download your VPN credentials and create new ones under the "devices" tab

Now it is time…
