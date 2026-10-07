# Azure Private Networking Lab

## Overview
Created two Ubuntu virtual machines in the same subnet
inside Sodiq-Vnet, without assigning public IP addresses
to either VM.

## My setup
- Virtual network: Sodiq-Vnet
- VM subnet: default — 10.0.0.0/24
- VM1 private IP: 10.0.0.4
- VM2 private IP: 10.0.0.5
- Remote access: Azure Bastion

## What I did
1. Created the virtual network and subnet.
2. Deployed two Ubuntu VMs without public IP addresses.
3. Connected to VM1 through Azure Bastion.
4. Ran `ping 10.0.0.5` from VM1.
5. Received successful replies from VM2.

## What I learned
- VMs can communicate using private IP addresses.
- Bastion lets me access a VM without assigning it a public IP.
- The ping traffic travelled directly between the two VMs
  over the private network.
- Traffic leaving VM1 is outbound; that same traffic
  arriving at VM2 is inbound.
- Ping uses ICMP rather than TCP port 22 or 3389.

## Screenshots
Uploaded screenshots show the VM networking details,
subnets, Bastion configuration and successful ping test.
