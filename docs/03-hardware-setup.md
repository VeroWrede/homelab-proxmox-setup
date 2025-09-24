# Linux Installation and Hardware Update 

## Project Phase Update
**Status Change**: Discovered pre-existing Proxmox installation on salvaged drive
**Current Objective**: Network reconfiguration for existing Proxmox deployment

## Hardware Discovery and Resolution

### Initial Hardware Assessment
**Problem**: Dell OptiPlex 7050 purchased as complete system was missing a hard drive

**Solution**:
- Sourced compatible Hard drive from retired equipment stash with existing Linux/Proxmox installation
- Extra: Salvaged functional RAM 
- Hardware integration and compatibility verification

### Drive Installation Results
**Inherited Configuration**:
- Pre-existing Linux base system
- Proxmox VE hypervisor already installed
- Network configuration for deprecated subnet
- Requires IP address reconfiguration for current network topology

## Technical Challenges Overcome

### Challenge 1: Bootable Media Creation
**Issue**: Initial USB installation issues
- Problem: Downloaded bootable Ubuntu ISO installation no longer working
- Symptom: BIOS could detect USB but not boot from it

**Root Cause Analysis**:
- failed to access USB content

**Resolution Process**:
1. USB write protection removal via diskpart via cmd using the followin approach
```
diskpart
select disk X
attributes disk clear readonly
clean
create partition primary
active
format fs=fat32 quick
assign
exit
```
2. Installation of Ubuntu Server ISO deployment to USB using balenaEtcher

**Skills Demonstrated**:
- Hardware troubleshooting
- Understanding of boot media requirements
- Command-line disk management (diskpart)
- Professional USB creation tools usage

### Challenge 2: Network Infrastructure Planning
**Network Assessment Completed**:
- Main router interface access and configuration established
- Device inventory and IP address range analysed
- DHCP scope planning for lab environment to avoid interfering with other users
- Reserved IP range allocation for this project  

**Technical Implementation**:
- Router admin interface navigation
- Network device identification and categorization
- IP address space management
- Network segmentation planning for personal projects and the rest of the household

### Challenge 3: Installation Environment Constraints
**Logistical Challenge**:
- Headless server installation requirements
- Physical workspace limitations required device relocation
- Network connectivity loss after relocation

**Adaptive Solutions**:
- Installed Ubuntu Server offline 
- Flexible installation approach to accommodate to workspace constraints
- Post-installation network configuration strategy

## Current System Status

### Hardware Configuration
- **Host**: Dell OptiPlex Micro Tower
- **RAM**: Salvaged more from decommissioned server (compatible)
- **Storage**: Existing drive from decommissioned server (compatible) with Proxmox VE already installed

### Software Stack
- **Base OS**: Linux (pre-installed)
- **Hypervisor**: Proxmox VE (operational, still needs network configuration update)
- **Current State**: System is working but network configuration is outdated

### Network Requirements
- **Current Config**: Static IP for past subnet
- **Target Config**: Static IP within main router's reserved range
- **Reserved Range**: Allocated specific IP range for lab projects
- **Next Phase**: IP address reconfiguration and connection to main router

## Skills and Technologies Applied

### Technical Skills Demonstrated
- **Hardware Diagnostics**: Component identification (faulty and functional) and compatibility check
- **System Assembly**: Drive and RAM installation and hardware integration
- **BIOS Configuration**: Boot order management and hardware detection
- **Network Planning**: IP address space management and router configuration
- **Problem Solving**: Adaptive approaches to hardware and logistical constraints
- **Command Line Operations**: Advanced disk management and troubleshooting
- **Documentation**: Comprehensive technical process documentation

### Tools and Technologies Used
- **Hardware**: Dell OptiPlex enterprise hardware 
- **Software**: Ubuntu Server, Proxmox VE, balenaEtcher
- **Network**: DHCP/static IP configuration, router administration
- **Command Line**: diskpart, network diagnostics, system administration

## Project Value and Learning Outcomes

### Real-World Experience Demonstrated
- **Hardware Failure Recovery**: Successful project continuation despite missing components
- **Resource Management**: Effective use of available hardware inventory
- **Adaptive Problem Solving**: Multiple solution paths for technical challenges
- **Infrastructure Planning**: Network design and IP address management
- **Documentation Practices**: Professional-grade technical documentation

### Enterprise Skills Applied
- **Server Hardware Management**: Enterprise desktop repurposing
- **Virtualization Platform Deployment**: Proxmox hypervisor administration
- **Network Infrastructure**: Router configuration and IP space management
- **Project Management**: Phase-based approach with adaptive planning
- **Technical Communication**: Clear documentation of complex procedures

## Next Steps: Network Configuration
**Immediate Objectives**:
1. Update existing Proxmox installation
2. Reconfigure network settings for new subnet
3. Establish remote management connectivity
4. Document network configuration process

**Success Metrics**:
- Proxmox web interface is accessible
- Network connectivity restored
- SSH access configured
- Documentation updated with network configuration process