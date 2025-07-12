# How to connect to OpenVPN
1. ```ip a | grep tun0```: check if you're connected
    - If IP address returned in form of ```10.10.X.X```, you're already connected! Disconnect first to connect to a different VPN.
2. ```sudo openvpn ~/Downloads/yourfile.ovpn```: connect to new VPN. Replace ```~/Downloads/yourfile.ovpn``` with your actual VPN config file.

# How to disconnect from OpenVPN
1. ```sudo pkill openvpn```: immediately disconnects you
2. ```ip a | grep tun0```: checks if you are actually disconnected
    - If no output is returned, you are disconnected.
3. ```sudo systemctl restart networking```: if ```tun0``` still returns IP address, reboot.

# How to check if you're connected
- Are you connected to a VPN? ```ip a | grep tun0```
  - If you see something like ```10.10.X.X```, you're connected!
- Can you ping the machine's IP? ```ping -c 4 <HTB-Machine-IP>```
- Did you add the machine to /etc/hosts? ```cat /etc/hosts```

# Troubleshooting
