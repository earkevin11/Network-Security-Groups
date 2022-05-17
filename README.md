# Network-Security-Groups

# What is the purpose of NSGs?
- Provide a firewall like service using security rules.
- It filters traffic inbound and outbound for VMs.
- By default, when admins create a VM, it will create a NSG. The NSG will attach to the NIC.
- Each rules have a priority and the lowest value will be applied.

# Important
- Note: By default, there is no inbound rule to allow traffic from the internet to the VM!
- Rules in NSG must be created to allow inbound traffic
- NSGs can be attached on the NIC or the subnet that contains the azure VMs.
- <em> You cannot apply NSG onto the entire virtual network. </em>
