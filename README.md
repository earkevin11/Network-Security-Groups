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



