# Network Infrastructure Troubleshooting

## Initial Network Plan
Main Router → Ethernet Switch → Secondary Router → Dell OptiPlex

## Issues Encountered
### Problem 1: Switch Failure
Symptoms:
- NETGEAR router showing "Not Connected" to internet
- Loss of internet connectivity when connected to secondary network
- The rest of the system component worked independently

Diagnosis Process:
- Verified physical connections
- Checked router admin interface
- Identified failed ethernet switch:
        - Device warm/hot to touch
        - No status indicator lights
        - Power adapter overheating

Root Cause: Hardware failure of 5-port ethernet switch

### Problem 2: Router Hardware Issues
Symptoms:
- Failed direct connection attempt
- Ethernet port on NETGEAR router non-functional

Diagnosis Process:
- Identified failed ethernet switch

Assessment: Multiple hardware failures requiring equipment replacement

## Solution Implemented
### Phase 1: Direct Connection Approach
Configuration:
- Main Router → Ethernet Cable → Dell OptiPlex
- Simplified network topology
- Eliminated potential failure points

Benefits:
- Immediate project continuation
- Reduced complexity for initial setup
- Foundation for future network expansion

Key considerations:
- Get main router's IP address
- Avoid using IP address already in use by other devices on the network


## Lessons Learned
- Always test hardware before integration
- Maintain flexible project planning for equipment failures
- Document troubleshooting processes for future reference
- Phased implementation allows for iterative improvement

## Future Enhancements
- Replace/repair secondary router equipment
- Implement network segregation in Phase 2
- Add managed switch for advanced VLAN configuration

## Technical Skills Demonstrated
- Hardware failure diagnosis
- Network connectivity troubleshooting
- Adaptive project management
- Documentation of technical challenges