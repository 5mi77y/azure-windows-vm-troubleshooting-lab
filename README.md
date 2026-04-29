# Azure Windows VM Connectivity Troubleshooting Lab

## Project Overview

This lab simulates a basic IT support troubleshooting scenario using Microsoft Azure and a Windows Server virtual machine.

The goal is to create a cloud-hosted Windows server, connect to it using Remote Desktop Protocol (RDP), intentionally break the connection by changing network access rules, then troubleshoot and restore access.

## Tools Used

- Microsoft Azure
- Windows Server 2025 Datacenter
- Windows App / Remote Desktop on macOS
- GitHub for documentation

## Baseline Setup

- Created a Windows Server virtual machine in Microsoft Azure.
- VM name: `win-it-lab-01`
- Resource group: `rg-it-lab-01`
- Region: Canada Central
- VM size: `Standard_B2als_v2`
- Connected from a MacBook Air M1 using the Windows App.
- Confirmed successful RDP access to the Windows Server desktop.

## Issue Simulated

The RDP connection will be intentionally broken by modifying the inbound network rule for TCP port 3389.

## Troubleshooting Process

To be completed after testing.

## Resolution

To be completed after restoring access.

## Key Learning

This lab demonstrates basic cloud infrastructure setup, remote access, network security rules, and troubleshooting methodology.
