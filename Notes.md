## Baseline network rule

- Inbound rule name: RDP
- Priority: 300
- Port: TCP 3389
- Source: Any
- Destination: Any
- Result: RDP connection works successfully
## Pre-change connection test

- VM status: Running
- Connection method: Windows App / RDP
- Result: Successfully connected to Windows Server
- Conclusion: RDP access works before modifying the network security rule
  
## Next test

- Delete the inbound RDP rule.
- Attempt to reconnect using Windows App / RDP.
- Expected result: connection fails because TCP 3389 is no longer allowed through the network security group.
