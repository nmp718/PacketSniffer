# Readme for .cap file used with Bettercap

This .cap file is used with Bettercap. The code in this file enables the user to perform an ARP spoofing attack and DNS spoofing attack on a specific target.
The goal of this script is to easily attack a device on a local network, and receive the target's network traffic.

## How it works
The program first enables the `net.probe` function to detect all devices on the network. Then, the `arp.spoof.fullduplex` and `dns.spoof.all` functions are turned on to enable full duplex ARP spoofing and DNS spoofing on all targets.

The program then waits for 6 seconds before displaying the network details with `net.show`. The user is prompted to select the target machine for the ARP spoofing attack using the `read arp.spoof.targets` command.

The user is then prompted to select the DNS server IP address with `read dns.spoof.address`. Next, the user is prompted to enter the domain names they want to spoof with `read dns.spoof.domains`.

After a 2-second pause, the program turns on the `arp.spoof` and `dns.spoof` functions to initiate the attacks.

## How to run with Bettercap
To use this .cap file with Bettercap, follow these steps:

1. Run Bettercap as a root user using the command, and use the .cap script `sudo bettercap -caplet /path/to/file`.
2. Follow the on-screen prompts to select the target machine, DNS server IP address, and domain names to spoof.
3. The ARP and DNS spoofing attacks will be initiated automatically.
