# Network-Security-Groups

# What is the purpose of NSGs?
- Provide a firewall like service using security rules.
- It filters traffic inbound and outbound for VMs.
- By default, when admins create a VM, it will create a NSG. The NSG will attach to the NIC.
- Each rules have a priority and the lowest value will be applied.

# Important
- Note: By default, there is no inbound rule to allow traffic from the internet to the VM!
- Example: if a user wants to RDP into a VM, a inbound rule will need to be created within the NSG.
- Rules in NSG must be created to allow inbound traffic
- NSGs can be attached on the <em> NIC </em> or the <em> subnet </em> that contains the azure VMs.
- <em> You cannot apply NSG onto the entire virtual network. </em>

# Remember: Traffic flows via the Network Interface (NIC) to the Virtual Machine, which is why the NSG is attached at the NIC level. 
- Think *NSG* = *Firewall*

# How to use NSGs?
- Go to VM > Networking > Select the NSG
- Inbound rules are used for traffic that flows into the VM
- Outbound rules are used for traffic that flows out of the VM
- Admins can associate NSGs with multiple subnets and NIC.
# There are 3 default rules created in NSG inbound rules
- 1. Allow all traffic within a VNet. This means if a VM tries to contact another VM within the same VNet. It will be allowed.
- 2. Allow traffic onto a Azure Load Balancer
- 3. All other traffic is denied inbound.

# Outbound Traffic rules
- 3 default rules in place
- 1. Allow Vnet outbound if destination is in the same VNet
- 2. Allow all internet outbound traffic
- 3. Deny all other outbound traffic

# Default inbound security rules
- Remeber that by default, users cannot RDP into a VM
- The warning sign at the RDP rule signals that admins should not allow everybody to RDP into the VM.
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/168944457-62c786fc-da63-4ecd-831e-fe6e510ce4df.png" height="290%" width="290%" alt="review of vnets and VMs"/>

<p/>


# Default outbound security rules
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/168944519-8c59e200-8fbb-44c7-8a62-0e3296384a85.png" height="290%" width="290%" alt="review of vnets and VMs"/>

<p/>


