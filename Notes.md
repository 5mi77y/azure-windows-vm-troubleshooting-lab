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

## Failed connection test

- Change made: Deleted the inbound RDP rule from the Network Security Group.
- Connection method: Windows App / RDP
- Result: Unable to connect
- Error code: 0x204
- Conclusion: The VM is still running, but RDP access fails because TCP port 3389 is no longer allowed through the Network Security Group.

## Fix applied

- Change made: Recreated the inbound RDP rule in the Network Security Group.
- Rule name: RDP
- Port: TCP 3389
- Source: Any
- Destination: Any
- Action: Allow
- Result: RDP connection restored successfully.
- Conclusion: Restoring the inbound TCP 3389 rule allowed RDP traffic back into the VM.

## Root cause

The RDP connection failed because the Network Security Group no longer had an inbound rule allowing TCP traffic on port 3389.

## Resolution

Recreating the inbound RDP rule restored access to the Windows Server VM.
