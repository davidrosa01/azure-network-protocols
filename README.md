<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4
- 

<h2>Actions and Observations</h2>

<p>
<img width="80%" height="80%" alt="imcmp" src="https://github.com/davidrosa01/davidrosa01/assets/119774564/73ef35c3-9a81-4072-96f1-c3518def2373">
</p>
<p>
In this section, we used Wireshark to observe ICMP traffic in Azure Virtual Machines. We pinged the Ubuntu VM from the Windows 10 VM, monitored the traffic in Wireshark, and tested connectivity to a public website. We also explored the impact of Network Security Groups by disabling and re-enabling ICMP traffic, observing the effects in Wireshark and the command line. These experiments provided practical insights into monitoring network traffic and the role of NSGs in securing Azure VMs.
</p>
<br />

<p>
<img width="80%" height="80%" alt="ssh" src="https://github.com/davidrosa01/davidrosa01/assets/119774564/3f5a44c0-8f11-4b3f-aada-74da7978f2ae">
</p>
<p>
In Wireshark, we focused on observing SSH traffic within the Azure Virtual Machines. By filtering for SSH traffic, we narrowed down the captured packets to specifically analyze SSH communication. Using the Windows 10 VM, we established an SSH connection to the Ubuntu Virtual Machine using its private IP address. Throughout the SSH session, we monitored the traffic in Wireshark, witnessing a stream of SSH packets being captured. To conclude the SSH session, we simply typed 'exit' within the SSH connection and pressed [Enter]. Through this process, we gained insights into monitoring SSH traffic and its corresponding packets in Wireshark, further enhancing our understanding of secure remote access in Azure Virtual Machines.
</p>
<br />

<p>
<img width="80%" height="80%" alt="dhcp" src="https://github.com/davidrosa01/davidrosa01/assets/119774564/5a3c6c6c-f089-408f-9428-437935b654be">
</p>
<p>
To observe DHCP traffic using Wireshark, we applied a filter specifically for DHCP packets. From the Windows 10 VM, we executed the command "ipconfig /renew" in the command line, aiming to acquire a new IP address through DHCP. As this command ran, we closely monitored the DHCP traffic in Wireshark. The captured packets revealed the DHCP communication, including the exchange of messages between the Windows 10 VM and the DHCP server. By analyzing this traffic, we gained valuable insights into the DHCP process and the associated packet-level details. This experiment allowed us to deepen our understanding of how IP address assignment occurs within the network environment.
</p>
<br />


<p>
<img width="80%" height="80%" alt="dhs" src="https://github.com/davidrosa01/davidrosa01/assets/119774564/34d67515-68f9-4e57-813e-ed1712ec57c6">
</p>
<p>
To observe DNS traffic in Wireshark, we applied a filter specifically for DNS packets. From the command line of the Windows 10 VM, we used the nslookup command to query the IP addresses of google.com and disney.com. While the nslookup commands were executed, we closely monitored the DNS traffic in Wireshark. The captured packets revealed the DNS communication, including the exchange of queries and responses between the Windows 10 VM and the DNS server. By analyzing this traffic, we gained insights into the DNS resolution process and the associated packet-level details. This experiment allowed us to deepen our understanding of how domain names are translated into IP addresses through DNS.
</p>
<br />


<p>
<img width="80%" height="80%"alt="rdp" src="https://github.com/davidrosa01/davidrosa01/assets/119774564/897c64f8-99b7-4998-af5a-f7b67e3efba8">
</p>
<p>
RDP traffic in Wireshark is characterized by a constant stream of data. Unlike other protocols that show traffic only during specific activities, RDP continuously transmits data to maintain a real-time live stream of desktop activity. This persistent traffic ensures synchronization between the local and remote machines, allowing immediate reflection of changes on the remote desktop. The continuous flow of RDP traffic is fundamental to its purpose of providing seamless and interactive remote desktop access.
</p>
<br />
